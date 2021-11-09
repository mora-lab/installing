<img src="https://github.com/mora-lab/mora-lab.github.io/blob/master/picture/MORALAB_Banner.png">

# Installing neo4j

> Neo4j has two different community (free) servers: the versions with the tag `4.+` support multiple databases in one server, while the versions with the tag `3.+` only support one database in one server. Here we will describe the installation of `neo4j 3.5.28` and `neo4j 4.3.2`.

## Installing neo4j on Windows:

### - Requirements:

> 1. Install **java 11** on Windows. You can follow our tutorial here: https://github.com/mora-lab/installing/tree/main/java

### - Installing neo4j 3.5.28:

> 1. Download neo4j 3.5.28 from https://neo4j.com/download-center/#community

<br><img src="images/image-20210714165119253.png" alt="image-20210714165119253" style="zoom:67%;" />

> 2. Uncompress the downloaded file [neo4j-community-3.5.28-windows.zip](neo4j-community-3.5.28-windows.zip) to your hard drive (here, `D:`).

<br><img src="images/image-20210714170404902.png" alt="image-20210714170404902" style="zoom:67%;" />

> 3. In the installation directory, you'll find:

* **bin** - scripts and other executables

* **conf** - server configuration

* **data** - databases

* **lib** - libraries

* **plugins** - user extensions

* **logs** - log files

* **import** - location of files for LOAD CSV

> 4. Open a terminal and, in the command line, introduce the following commands to run **neo4j**:

```shell
D:
cd neo4j-community-3.5.28\bin
neo4j.bat console
```

<br><img src="images/image-20210714170849613.png" alt="image-20210714170849613" style="zoom:67%;" />

**If you want to stop neo4j, just press `Ctrl + C`.**

> 5. In a browser, open http://localhost:7474/

<br><img src="images/image-20210714171419767.png" alt="image-20210714171419767" style="zoom:67%;" />

> 6. Connect using the username 'neo4j' and the default password 'neo4j'. You'll then be prompted to change the password.

<br><img src="images/image-20210714171538944.png" alt="image-20210714171538944" style="zoom:67%;" />

> 7. The following is a view of the neo4j browser:

<br><img src="images/image-20210714171916505.png" alt="image-20210714171916505" style="zoom:50%;" />

> Neo4j browser includes several practices for beginners.

<br><img src="images/image-20210714172001739.png" alt="image-20210714172001739" style="zoom:50%;" />
<br><img src="images/image-20210714172024658.png" alt="image-20210714172024658" style="zoom:50%;" />
<br><img src="images/image-20210714172056992.png" alt="image-20210714172056992" style="zoom:50%;" />

## - Installing neo4j 4.3.2:

> 8. Downlaod [neo4j 4.3.2](https://neo4j.com/artifact.php?name=neo4j-community-4.3.2-windows.zip) from https://neo4j.com/download-center/#community

<br><img src="images/image-20210712171141256.png" alt="image-20210712171141256" style="zoom:67%;" />

> 9. Uncompress the downloaded file [neo4j-community-4.3.2-windows.zip](neo4j-community-4.3.2-windows.zip) to your hard drive (here, `D:`).

<br><img src="images/image-20210712171445597.png" alt="image-20210712171445597" style="zoom:67%;" />

> 10. Open a terminal and, in the command line, introduce the following commands to run **neo4j**:

```shell
# go to the bin directory of neo4j-community
D:
cd D:\neo4j-community-4.3.2\bin

# run neo4j
neo4j.bat console
```

<br><img src="images/image-20210712172242628.png" alt="image-20210712172242628" style="zoom:67%;" />

> **If you want to stop running neo4j, press `Ctrl + C`.**

> 11. In a browser, open http://localhost:7474/

<br><img src="images/image-20210712172427079.png" alt="image-20210712172427079" style="zoom:67%;" />

> 12. Connect using the username 'neo4j' and the default password 'neo4j'. You'll then be prompted to change the password.

<br><img src="images/image-20210712172520981.png" alt="image-20210712172520981" style="zoom:67%;" />

> 13. The following is a view of the neo4j browser:

<br><img src="images/image-20210712172810394.png" alt="image-20210712172810394" style="zoom:50%;" />

### - Installing neo4j with Docker:

> To know more about Docker, see our tutorial: https://github.com/mora-lab/installing/tree/main/docker
> Docker installation instructions can be found at https://docs.docker.com/get-docker/.

#### - A few notes on Docker Containers, Images and Registry:

- Containers are the running Images
- Changes in a Container will not change anything in the Images
- Registry (docker hub) is the storage of the images in the cloud
- One image can have many Containers, but one container is only for one image
- `docker build ` is the command for building an Image
- `docker pull` is the command for downloading an image from the Registry
- `docker run` is for running the image as a container

<br><img src="images/architecture.svg" alt="architecture" style="zoom:80%;" />

#### - Docker Commands Diagram:

<br><img src="images/cmd_logic.png" alt="cmd_logic" style="zoom:80%;" />

> 14. The neo4j docker official Images can be found here: https://hub.docker.com/_/neo4j

> The raw files for building the neo4j images can be found here: https://github.com/neo4j/docker-neo4j

> 15. If we only want to download the neo4j image, we can use:
```shell
docker pull neo4j
```
> By default, this will download the neo4j with the 'latest' tag.

<br><img src="images/image-20210716125322630.png" alt="image-20210716125322630" style="zoom:80%;" />

> If we want to download neo4j with a special tag (for example, download neo4j 3.5.29-community):
```shell
docker pull neo4j:3.5.29-community
```

<br><img src="images/image-20210716125428733.png" alt="image-20210716125428733" style="zoom:80%;" />

> More neo4j images can be found at https://hub.docker.com/_/neo4j?tab=tags&page=1&ordering=last_updated

> 16. List all images.

```shell
docker images
```

<br><img src="images/image-20210716140753556.png" alt="image-20210716140753556" style="zoom:80%;" />

> - **REPOSITORY**: the image name
> - **TAG**: the image version
> - **IMAGE ID**: the image ID
> - **CREATED**: create time
> - **SIZE**: the image size

> 17. Run **neo4j**.

```shell
# run neo4j, default run the neo4j with latest Tag
docker run \
    --publish=7474:7474 --publish=7687:7687 \
    --volume=$HOME/neo4j/data:/data \
    --name neo4j-docker-test \
    neo4j
```

> - `--publish` sets the port. The first `7474` is the port of the host, while the second `:7474` is the port of the container. By default, we do not change the second `:7474`. If you don't want to use `7474` of the host to set neo4j browser, you can set it as `--publish=4545:7474` to make `4545` as the port.
> - `--volume` is the argument to set a directory bound to the directory of the container. `--volume=$HOME/neo4j/data:/data` set the `/data` of the container bound to `$HOME/neo4j/data` of the host. That means, if you change anything in the `/data` of the container, `$HOME/neo4j/data` of the host will also change. In the same way, if there is a change in the `$HOME/neo4j/data` of the host, there will be a change in the `/data` of the container.
> - `--name neo4j-docker-test` is setting the container's name (`neo4j-docker-test`).
> - `neo4j` is the image name. If you want to run neo4j with a special tag, just use `neo4j:<tag>`. For example: `neo4j:3.5.29-community`

<br><img src="images/image-20210716132553080.png" alt="image-20210716132553080" style="zoom:80%;" />

> Press `CTRL + C` to stop this neo4j container.

> 18. After running, a `neo4j/data` folder will appear in the host.

<br><img src="images/image-20210716140635395.png" alt="image-20210716140635395" style="zoom:67%;" />

> If you want to run neo4j in the backgroud, you need to add the `-d` argument:

```shell
docker run \
    --publish=7474:7474 --publish=7687:7687 \
    --volume=$HOME/neo4j/data:/data \
    -d \
    --name neo4j-docker \
    neo4j
```

<br><img src="images/image-20210716140714670.png" alt="image-20210716140714670" style="zoom:80%;" />

> 19. Visit http://localhost:7474/ or http://host-ip:7474 .

> If you want to access http://host-ip:7474 , you should open the `7474` port of the firewall in the host.

<br><img src="images/image-20210716134337055.png" alt="image-20210716134337055" style="zoom:67%;" />

> 20. Check the running neo4j or List all running containers:

```shell
# Check the running neo4j
# List all running containers
docker ps 
```

<img src="images/image-20210716141214691.png" alt="image-20210716141214691" style="zoom:80%;" />

- **CONTAINER ID**: the container ID
- **IMAGE**: the image for this container
- **COMMAND** command to run this container
- **CREATED**:  creation time
- **STATUS**: the container's status
- **PORTS**: which ports exposed and can be accessed
- **NAME**: the container's name

> 21. A few basic operations with neo4j containers:

> List all containers:
```shell
# List all containers
docker ps -a
```
<br><img src="images/image-20210716141756599.png" alt="image-20210716141756599" style="zoom:67%;" />

> Remove a container:
```shell
# Remove the container named neo4j-docker-test
docker rm -f neo4j-docker-test
```
> Here, `interesting_shirley` is the container name, but you can set a special name with `--name` in `docker run`.
> The second way to delete a container is using `docker rm -f <containerID>`.
**Note:** You need to save your data before delete the container.
<br><img src="images/image-20210716142057406.png" alt="image-20210716142057406" style="zoom:67%;" />

> Checking the files inside the container:
```shell
# docker exec -it <containerID> <command>
# docker exec -it <containerNAME> <command>
docker exec -it neo4j-docker bash
```
<br><img src="images/image-20210716142709751.png" alt="image-20210716142709751" style="zoom:67%;" />
**Use `exit` to exit the container.**

> Stop the neo4j container:
```shell
# docker stop <containerID>
# docker stop <containerNAME>
docker stop neo4j-docker
```
<br><img src="images/image-20210716143353059.png" alt="image-20210716143353059" style="zoom:67%;" />

> Start the neo4j container:
```shell
# docker start <containerID>
# docker start <containerNAME>
docker start neo4j-docker
```
<br><img src="images/image-20210716143439345.png" alt="image-20210716143439345" style="zoom:67%;" />

> Restart the neo4j container:
```shell
# docker restart <containerID>
# docker restart <containerNAME>
docker restart neo4j-docker
```
**Note: when you start/restart the container, the container must exist.**

> Remove all containers:
```shell
docker rm -f $(docker ps -aq)
```
**Note: You need to save your data before deleting the container.**

> Remove all images:
```shell
docker rmi -f $(docker images -aq)
```

### - neo4j configuration:

> 22. Neo4j configuration can set in the file `$NEO4J_HOME/conf/neo4j.conf`.

#### The default database:

> 23. Neo4j database will be pulled in the `$NEO4J_HOME/data/databases` directory.

> `Neo4j 4.+`:
```yaml
# The name of the default databases
dbms.default_database=neo4j
```

> `Neo4j 3.+`:
```R
# The name of the database to mount
dbms.active_database=graph.db
```

#### Set the maximum memory:

```yaml
# Java Heap Size: by default the Java heap size is dynamically
# calculated based on available system resources.
# Uncomment these lines to set specific initial and maximum
# heap size.
dbms.memory.heap.initial_size=512m
dbms.memory.heap.max_size=512m

# The amount of memory to use for mapping the store files.
# The default page cache memory assumes the machine is dedicated to running

# Neo4j, and is heuristically set to 50% of RAM minus the Java heap size.
dbms.memory.pagecache.size=10g

# Limit the amount of memory that all of the running transaction can consume.
# By default there is no limit.
dbms.memory.transaction.global_max_size=256m

# Limit the amount of memory that a single transaction can consume.
# By default there is no limit.
dbms.memory.transaction.max_size=16m
```

> In this tutorial, we use more memory than the default.

```yaml
# For example, we set memory is 10GB
dbms.memory.heap.initial_size=10g
dbms.memory.heap.max_size=10g
```

#### Default directory for `LOAD CSV`:

> 24. Default directory for `LOAD CSV` is `$NEO4J_HOME/import`.

```yaml
# This setting constrains all `LOAD CSV` import files to be under the `import` directory. Remove or comment it out to
# allow files to be loaded from anywhere in the filesystem; this introduces possible security problems. See the
# `LOAD CSV` section of the manual for details.
dbms.directories.import=import
```

### - Network configuration:

> 25. Remote access:

```yaml
# With default configuration Neo4j only accepts local connections.
# To accept non-local connections, uncomment this line:
dbms.connectors.default_listen_address=0.0.0.0
```

> 26. Change the port:

```yaml
# Bolt connector
dbms.connector.bolt.enabled=true
#dbms.connector.bolt.tls_level=OPTIONAL
dbms.connector.bolt.listen_address=:7687

# HTTP Connector. There can be zero or one HTTP connectors.
dbms.connector.http.enabled=true
dbms.connector.http.listen_address=:7474

# HTTPS Connector. There can be zero or one HTTPS connectors.
dbms.connector.https.enabled=true
dbms.connector.https.listen_address=:7473
```

> 27. Neo4j worker threads：

```yaml
# Number of Neo4j worker threads.
#dbms.threads.worker_count=
```

### - Plugins configuration:

> 28. Plugins should be put in the folder `$NEO4J_HOME/plugins`.

```yaml
# A comma separated list of procedures and user defined functions that are allowed
# full access to the database through unsupported/insecure internal APIs.
#dbms.security.procedures.unrestricted=my.extensions.example,my.procedures.*

# A comma separated list of procedures to be loaded by default.
# Leaving this unconfigured will load all procedures found.
#dbms.security.procedures.whitelist=apoc.coll.*,apoc.load.*
```

> Example: add `apoc` and `algo` plugins.

```yaml
dbms.security.procedures.unrestricted=algo.*,apoc.*
```

### - Only allow read operations from this Neo4j instance:

```yaml
# Only allow read operations from this Neo4j instance. This mode still requires
# write access to the directory for lock purposes.
#dbms.read_only=false 
```

> only Allow read operations set it as:

```yaml
dbms.read_only=true
```

## Installing neo4j on Linux CentOS:

### - First steps
* Open Linux
* Verify Internet connection
* Install java 11 for Linux CentOS: https://github.com/mora-lab/installing/tree/main/java

### - Install cypher-shell:
```
curl -O https://dist.neo4j.org/cypher-shell/cypher-shell-4.2.2-1.noarch.rpm
sudo rpm -U cypher-shell-4.2.2-1.noarch.rpm
```

### - Install neo4j:
```
curl -O https://dist.neo4j.org/rpm/neo4j-4.2.2-1.noarch.rpm
sudo rpm -U neo4j-4.2.2-1.noarch.rpm
neo4j version	# 4.2.2
```

### - Start neo4j:
```
sudo systemctl daemon-reload
sudo neo4j start
```

> Open a web browser at localhost:7474

### - Connecting from outside:
> When connecting from the outside, set the following:
```
sudo vi /etc/neo4j/neo4j.conf
```
```
dbms.connector.bolt.address=0.0.0.0:7687
dbms.connector.https.address=<IP address of the server>:7474
```
> That will open the 7678 and 7474 ports.

## Installing our Docker neo4j:
> To install our Docker neo4j 3.5.4 with graphical plugins, which we use in our neo4j+shiny platform to study COPD, follow the instructions here:
https://hub.docker.com/r/moralab/neo4j-3.5.4

<br><img src="images/image-20210716142011100.png" alt="image-20210716142011100" style="zoom:67%;" />

*last reviewed: Nov.11th, 2021*
