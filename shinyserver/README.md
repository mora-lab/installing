<img src="https://github.com/mora-lab/mora-lab.github.io/blob/master/picture/MORALAB_Banner.png">

# Shiny Server

**Shiny server** is a tool to publish and manage shiny applications online.

> **Shiny Server** can manage R processes running various Shiny applications over different URLs and ports. Using **Shiny Server** offers multiple benefits over simply running Shiny in R directly, including:

> - Host multiple applications simultaneously, each at its own URL.
> - Support web browsers that don't support WebSocket, including Internet Explorer 8 & 9.
> - Enable system users to develop and manage their own Shiny applications.
> - Ensure that R processes that crash or are terminated automatically restart for the next user requesting the application.

The full manual can be found at https://docs.rstudio.com/shiny-server/.

## Installation

### Ubuntu

```shell
# install R
sudo apt-get install r-base

# install shiny
sudo su - \
-c "R -e \"install.packages('shiny', repos='https://cran.rstudio.com/')\""

# download and install
sudo apt-get install gdebi-core
wget https://download3.rstudio.org/ubuntu-14.04/x86_64/shiny-server-1.5.17.973-amd64.deb
sudo gdebi shiny-server-1.5.17.973-amd64.deb
```

### RedHat/CentOS

```shell
# install R
sudo yum install R

# install shiny
sudo su - \
-c "R -e \"install.packages('shiny', repos='https://cran.rstudio.com/')\""

# download
wget https://download3.rstudio.org/centos7/x86_64/shiny-server-1.5.17.973-x86_64.rpm

# install 
sudo yum install --nogpgcheck shiny-server-1.5.17.973-x86_64.rpm
```

> More details at https://www.rstudio.com/products/shiny/download-server/redhat-centos/.

## Starting and Stopping

```shell
# start shiny-server
sudo systemctl start shiny-server

# stop shiny-server 
sudo systemctl stop shiny-server

# restart shiny-server
sudo systemctl restart shiny-server

# check the status of the shiny-server
sudo systemctl status shiny-server

# enable shiny-server
sudo systemctl enable shiny-server

# disable shiny-server
sudo systemctl disable shiny-server
```

## Server Management

If you want to import a shiny App to the shiny server, you can set it in the configuration file.

As default, shiny server uses the following configuration file (which is found at `/etc/shiny-server/shiny-server.conf`):

```yaml
# Define the user we should use when spawning R Shiny processes
run_as shiny;

# Define a top-level server which will listen on a port
server {
  # Instruct this server to listen on port 3838
  listen 3838;

  # Define the location available at the base URL
  location / {
    #### PRO ONLY ####
    # Only up tp 20 connections per Shiny process and at most 3 Shiny processes
    # per application. Proactively spawn a new process when our processes reach 
    # 90% capacity.
    utilization_scheduler 20 .9 3;
    #### END PRO ONLY ####

    # Run this location in 'site_dir' mode, which hosts the entire directory
    # tree at '/srv/shiny-server'
    site_dir /srv/shiny-server;
    
    # Define where we should put the log files for this location
    log_dir /var/log/shiny-server;
    
    # Should we list the contents of a (non-Shiny-App) directory when the user 
    # visits the corresponding URL?
    directory_index on;
  }
}

# Setup a flat-file authentication system. {.pro}
auth_passwd_file /etc/shiny-server/passwd;

# Define a default admin interface to be run on port 4151. {.pro}
admin 4151 {
  # Only permit the user named `admin` to access the admin interface.
  required_user admin;
}
```

### Who runs the shiny Application?

As default, the shiny Application is run by the shiny user. If you want to use a different user (example: tim), you can set:

```shell
location / {
  run_as tim;
}
```

### R packages for the shiny Application

When you use the `shiny` user to run the shiny application, you should install R packages with that `shiny` user.

### Define port

The default port for the shiny server is `3838`. If you want to set `80` as the shiny server port, you can set:

```shell
server {
  listen 80;
}
```

### Location

The `location` setting is defined within a `server` and defines how a particular URL path should be served. For instance, the following settings:

```shell
server {
  ...
  # Define the location '/specialApp'
  location /specialApp {
    # Run this location in 'app_dir' mode, which will host a single Shiny
    # Application available at '/srv/shiny-server/myApp'
    app_dir /srv/shiny-server/myApp;
  }
  
  # Define the location '/otherApps'
  location /otherApps {
    # Run this location in 'site_dir' mode, which hosts the entire directory
    # tree at '/srv/shiny-server/apps'
    site_dir /srv/shiny-server/apps;
  }
...
}
```

## Our own Docker shiny server image
The following are the instructions to get our Docker shiny server image, which has been used in our Neo4j+shiny platform to analyze COPD dynamic data.<br>

https://hub.docker.com/r/moralab/shiny-server

*Last updated: Oct.30th, 2021*
