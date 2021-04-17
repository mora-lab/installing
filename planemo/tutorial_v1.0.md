<img src="https://github.com/mora-lab/mora-lab.github.io/blob/master/picture/MORALAB_Banner.png">

# Installing Planemo
<br>

> The following are the instructions to install **Planemo** (version xxx) on Linux. The tutorial uses a **Linux CentOS-Stream-8** installed in a **VirtualBox 6.1.18** virtual machine. A similar procedure can be followed using other OS.

## - Before starting
<br>

> 1. In order to install Planemo, you must previously have installed python, Galaxy and R/Rstudio in a Linux environment.
If you don't have them installed yet, follow our tutorials:

[Creating a CentOS-Stream-8 VirtualBox VM](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v1.0.md)
[Installing Anaconda](https://github.com/mora-lab/installing/blob/main/anaconda/tutorial_v1.0.md)
[Installing Galaxy](https://github.com/mora-lab/installing/blob/main/galaxy/tutorial_v1.0.md)
[Installing Rstudio](https://github.com/mora-lab/installing/blob/main/rstudio/tutorial_v1.0.md)

> 2. Go to your Linux machine. In our case, open **VirtualBox** and start the VM. Open a terminal in your Linux environment.

## - Download and install
<br>

> 3. 
<br>
<img src="images/Anaconda01.PNG" width="600">
<br>
<img src="images/Anaconda02.PNG" width="600">
<br>

> 2. Open a terminal and download **Anaconda3** latest version (currently, 2020.11) using:
```
curl -O https://repo.anaconda.com/archive/Anaconda3-2020.11-Linux-x86_64.sh
```
<br>
<img src="images/Anaconda04.PNG" width="600">
<br>

## - Installing Anaconda
<br>

> 3. Run the downloaded file by using:
```
bash Anaconda3-2020.11-Linux-x86_64.sh
```
<br>
<img src="images/Anaconda05.PNG" width="600">
<br>

> 4. Follow the installation procedure (accept license, location, etc).
<br>
<img src="images/Anaconda06.PNG" width="600">
<br>
<img src="images/Anaconda07.PNG" width="600">
<br>
<img src="images/Anaconda08.PNG" width="600">
<br>
<img src="images/Anaconda09.PNG" width="600">
<br>

## - Activate python's base environment
<br>

> 5. Go to the *bin* folder and activate **Anaconda**'s base environment.
```
cd /home/username/anaconda3/bin
. ./activate
```
<br>
<img src="images/Anaconda10.PNG" width="600">
<br>

## - Check Anaconda's functionality
<br>

> 6. Test **python** version (3.8.5) and **Jupyter notebooks**.
<br>
<img src="images/Anaconda11.PNG" width="600">
<br>
<img src="images/Anaconda12.PNG" width="600">
<br>

> 7. Test **Jupyter Lab** and the **Anaconda Navigator**.
<br>
<img src="images/Anaconda13.PNG" width="600">
<br>
<img src="images/Anaconda14.PNG" width="600">
<br>
<img src="images/Anaconda15.PNG" width="600">
<br>
<img src="images/Anaconda16.PNG" width="600">
<br>

## - Deactivate
> 8. To leave the environment, use: `conda deactivate`
<br>
<img src="images/Anaconda17.PNG" width="600">
<br>

*Last updated: Antonio Mora, April 17th, 2021*
