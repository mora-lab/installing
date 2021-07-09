<img src="../mora-lab.github.io/picture/MORALAB_Banner.png">

# Installing Docker and Galaxy Docker Images
<br>

> The following are the instructions to install **Docker** (version 20.10.6) and Galaxy Docker images on Linux. The tutorial uses a **Linux CentOS-Stream-8** installed in a **VirtualBox 6.1.18** virtual machine, as described here: [Creating a CentOS-8 VM](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v1.0.md). A similar procedure can be followed using other OS.

## - Downloads
<br>

> 1. Go to your Linux machine. In our case, open the **VirtualBox**.
<br>
<img src="images/Anaconda01.PNG" width="600">
<br>

> 2. Create a new VM called **CentOS-Stream-8-Docker** with a "Dynamically allocated" hard disk (no fixed size; maximum size 300 GB) and the "Server with GUI" option (instead of Workstation), following the steps in the tutorial [Creating a CentOS-8 VM](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v1.0.md).

> 3. Open a terminal. Docker will go to the cs-root directory. Check the size of this folder.
```
df -h	# sudo lvdisplay
```

> 4. Connect to Internet. Install **python** using:
```
curl -O https://repo.anaconda.com/archive/Anaconda3-2020.11-Linux-x86_64.sh
```
<br>
<img src="images/Anaconda04.PNG" width="600">
<br>

> 5. Run the downloaded file by using:
```
bash Anaconda3-2020.11-Linux-x86_64.sh
```
<br>
<img src="images/Anaconda05.PNG" width="600">
<br>

> 6. Follow the installation procedure (accept license, location, etc).
<br>
<img src="images/Anaconda06.PNG" width="600">
<br>

## - Installing Docker
<br>

> Description: https://docs.docker.com/engine/install/centos/

> 7. Uninstall old versions:
```
sudo dnf remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine
```

> 8. Uninstall conflicts:
```
sudo dnf -y remove podman runc
```

> 9. Set up repository:
```
sudo dnf install -y yum-utils

sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo
```

> 10. Install latest **Docker** (currently, 20.10.6) and Containerd:
```
sudo dnf install docker-ce docker-ce-cli containerd.io
#If prompted to accept the GPG key, verify that the fingerprint matches 060A 61C5 1B55 8A7F 742B 77AA C52F EB6B 621E 9F35, and if so, accept it.

docker version	# (Here, 20.10.6)
```

> "Docker is installed but not started. The docker group is created, but no users are added to the group."

## - Start Docker:

> 11. Start Docker:
```
sudo systemctl start docker
```

> 12. Run the Hello world image (if it doesn't exist, it will be downloaded):
```
sudo docker run hello-world
```

> 13. (Optional). Uninstalling:
```
sudo yum remove docker-ce docker-ce-cli containerd.io
```
