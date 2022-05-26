<img src="https://github.com/mora-lab/mora-lab.github.io/blob/master/picture/MORALAB_Banner.png">

# Importing an existing Virtual Machine into VirtualBox
<br>

> The following are the instructions to import an existing virtual machine (VM) in **VirtualBox 6.1.34** for **Windows 10** (now referred as the "host" operative system).

## - Installing VirtualBox
<br>

> 1. If you haven't installed **VirtualBox**, first go to our tutorial to install it:

> [How to install VirtualBox](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v2.0a.md)

## - Importing a new Virtual Machine
<br>

> 2. Open **VirtualBox**. Instead of creating a new VM from scratch, as we learned [here](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v2.0b.md), we might need to import an existing virtual machine, with all its software and data. Two easy ways of doing that is by sharing a Virtual Disk Image (VDI) or an appliance (Open Virtualization format Archive, OVA).

## - Importing virtual disk images (VDI files):

> 3. Get your VDI file: You can find multiple VDIs on Internet (for example, at [OSBoxes](https://www.osboxes.org/virtualbox-images/), [Virtualboxes](https://virtualboxes.org/images/), or [VirtualDiskImages](http://virtualdiskimages.weebly.com/virtualbox.html)). For the purposes of this tutorial, download and unzip an image of [Zorin 16.1](https://www.osboxes.org/zorin-os/), which is another popular Linux distro. You may also want to try [CentOS9-workstation](https://www.osboxes.org/centos/), [CentOS9-server](https://www.osboxes.org/centos/), or [Deepin](https://www.osboxes.org/deepin/).

> 4. Open **Virtual Box** and create a VM following the initial steps of our [tutorial](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v2.0b.md).

<br>
<img src="images/VBox112.PNG" width="500">
<br>
<img src="images/VBox70.PNG" width="500">
<br>

> 5. After you give a name to the VM and assign memory (and before assigning disk space and installing the OS), move the downloaded VDI file inside the new VM folder (the name you just assigned).

<br>
<img src="images/VBox111b.PNG" width="500">
<br>

> 6. Continue the process of creating the virtual machine: choose "Use an existing virtual hard disk file", click on the small folder, and find your VDI file.

<br>
<img src="images/VBox113.PNG" width="500">
<br>
<img src="images/VBox114.PNG" width="500">
<br>
<img src="images/VBox115.PNG" width="500">
<br>
<img src="images/VBox116.PNG" width="500">
<br>
<img src="images/VBox117.PNG" width="500">
<br>

> 7. That's it. Double-click and run the new VM. (Note: For all OSboxes' VDIs, username=osboxes, password=osboxes.org, root account password=osboxes.org).

<br>
<img src="images/VBox118.PNG" width="500">
<br>
<img src="images/VBox119.PNG" width="500">
<br>
<img src="images/VBox120.PNG" width="500">
<br>

> 8. You might be prompted to update some of the software.

<br>
<img src="images/VBox121.PNG" width="500">
<br>

> 9. You have successfully created a Zorin-16.1 VM. If you find some problems, check the "Troubleshooting" section of our tutorial.

<br>
<img src="images/VBox122.PNG" width="500">
<br>

## - Importing appliances (OVA files):

> 9. First, get your OVA file. One example of OVA files that can be used in this tutorial is our [Galaxy-GSA](https://zenodo.org/record/5091267). Download the OVA file [here](https://zenodo.org/record/5091267/files/Galaxy-GSA.ova?download=1).

> 10. Open **Virtual Box**. In the *File* menu, select *Import Appliance* and then choose your OVA file.

<br>
<img src="images/VBox123.PNG" width="500">
<br>
<img src="images/VBox124.PNG" width="500">
<br>
<img src="images/VBox125.PNG" width="500">
<br>
<img src="images/VBox126.PNG" width="500">
<br>

> 11. You will get a box with the appliance settings. To avoid problems, use most of the default specifications. Just update your base folder.

<br>
<img src="images/VBox127.PNG" width="500">
<br>

> 12. Click on **Import**.

<br>
<img src="images/VBox128.PNG" width="500">
<br>

> 13. That's it. Double-click on your new VM.

<br>
<img src="images/VBox129.PNG" width="500">
<br>
<img src="images/VBox130.PNG" width="500">
<br>

> 14. The username is **galaxy** and the password is *galaxy*. Now you can use the VM: This is an Ubuntu Linux machine with Anaconda, Galaxy, and Galaxy-GSA installed. You can use it as an Ubuntu machine or you can follow the instructions in the screen to run Galaxy-GSA.

<br>
<img src="images/VBox131.PNG" width="500">
<br>
<img src="images/VBox132.PNG" width="500">
<br>
<img src="images/VBox134.PNG" width="500">
<br>

> 15. You might also get a software update message. If you just want to use the Galaxy-GSA, we don't recommend updates, as we know this is a stable configuration, while we don't know the effects of future updates.

<br>
<img src="images/VBox133.PNG" width="500">
<br>

*Last updated: Antonio Mora, May 23rd, 2022*
