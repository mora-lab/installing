<img src="https://github.com/mora-lab/mora-lab.github.io/blob/master/picture/MORALAB_Banner.png">

# Installing RStudio in Linux
<br>

> The following are the instructions to install **RStudio** on Linux. The tutorial uses a **Linux CentOS-Stream-8** installed in a **VirtualBox** virtual machine 6.1.18, as described here: [Creating a CentOS-8 VM](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v1.0.md). A similar procedure can be followed by other OS.

## - Download and install R
<br>

> 1. Go to your Linux machine. In our case, open the **VirtualBox** and start the VM.
<br>
<img src="images/Anaconda01.PNG" width="600">
<br>
<img src="images/Anaconda02.PNG" width="600">
<br>

> 2. Open a terminal and download **R**. There are several alternative ways to do this (using either *dnf*, *yum*, *conda*, and others), but here we wil use `conda`:
```
conda install R
```
<br>
<img src="images/Rstudio04.PNG" width="600">
<br>
<img src="images/Rstudio05.PNG" width="600">
<br>

> 3. Check R version (in our case, it is 3.5.1).
```
R --version
```
<br>
<img src="images/Rstudio06.PNG" width="600">
<br>

## - Download and install RStudio
<br>

> We have two options: Either downloading **RStudio-Desktop** or **RStudio-Server**. The code in each case is shown below but we will only follow the first case.
> 3. Run the downloaded file by using:
```
wget https://download1.rstudio.org/desktop/centos8/x86_64/rstudio-1.4.1106-x86_64.rpm
sudo yum install rstudio-1.4.1106-x86_64.rpm
```
```
wget https://download2.rstudio.org/server/centos8/x86_64/rstudio-server-rhel-1.4.1106-x86_64.rpm
sudo yum install rstudio-server-rhel-1.4.1106-x86_64.rpm
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

## - Activate Anaconda
<br>

> 5. Go to the *bin* folder and activate **Anaconda**.
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

*Last updated: Antonio Mora, April 8th, 2021*
