<img src="../../mora-lab.github.io/picture/MORALAB_Banner.png">

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

