<img src="https://github.com/mora-lab/mora-lab.github.io/blob/master/picture/MORALAB_Banner.png">

# Importing an existing Virtual Machine into VirtualBox
<br>

> The following are the instructions to import an existing virtual machine (VM) in **VirtualBox 6.1.34** for **Windows 10** (now referred as the "host" operative system) and install **CentOS-Stream-9** Linux system (now referred as the "guest" operative system). A similar process can be followed for other host and guest OS.

## - Installing VirtualBox
<br>

> 1. If you haven't installed **VirtualBox**, first go to our tutorial to install it:

> [How to install VirtualBox](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v2.0a.md)

## - Importing a new Virtual Machine
<br>

> 2. Open **VirtualBox**. Instead of creating a new VM from scratch, as we learned [here](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v2.0b.md), we might need to import an existing virtual machine, with all its software and data. Two easy ways of doing that is by sharing a Virtual Disk Image (VDI) or an appliance (Open Virtualization format Archive, OVA).

## - Importing virtual disk images (VDI files):

> 3. Get your VDI file: You can find multiple VDIs on Internet (for example, at [OSBoxes](https://www.osboxes.org/virtualbox-images/), [Virtualboxes](https://virtualboxes.org/images/), or [VirtualDiskImages](http://virtualdiskimages.weebly.com/virtualbox.html)). For the purposes of this tutorial, download and unzip an image of [Lubuntu 20.04.1](https://sourceforge.net/projects/osboxes/files/v/vb/33-Lb--t/20.04.1/L20.04.1-VB-64bit.7z/download), which is a lightweight version of Ubuntu Linux.

> 4. Open **Virtual Box** and create a VM following the steps 1-8 of our [tutorial](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v2.0b.md).

<br>
<img src="images/d01.PNG" width="600">
<br>
<img src="images/d02.PNG" width="600">
<br>

> 5. After you give a name to the VM and assign memory (and before assigning disk space and installing the OS), move the VDI file inside the new VM folder (the name you just assigned).

> 6. When you are in the "Create virtual machine/Hard disk" step, choose "Use an existing virtual hard disk file", click on the small folder, and find your VDI file.

<br>
<img src="images/d03.PNG" width="600">
<br>

> 7. Double-click and run the new VM.

<br>
<img src="images/d04.PNG" width="600">
<br>
<img src="images/d05.PNG" width="600">
<br>

> 8. Type the password and that's it. (Note: For all OSboxes' VDIs, username=osboxes, password=osboxes.org, root account password=osboxes.org).

<br>
<img src="images/d06.PNG" width="600">
<br>

## - Importing appliances (OVA files):

> 9. First, get your OVA file. One example of OVA files that can be used in this tutorial is our [Galaxy-GSA](https://www.zenodo.org/53095). Download the OVA file [here](https://www.zenodo.org/53095.ova).

> 10. Open **Virtual Box**. In the *File* menu, select *Import Appliance* and then choose your OVA file.

<br>
<img src="images/e01.PNG" width="600">
<br>
<img src="images/e02.PNG" width="600">
<br>

> 11. You will get a box with the appliance settings. To avoid problems, uncheck all the controllers and update your base folder.

<br>
<img src="images/e03.PNG" width="600">
<br>
<img src="images/e03b.PNG" width="600">
<br>

> 12. Click on **Import**.

<br>
<img src="images/e04.PNG" width="600">
<br>

> 13. Double-click on your new VM.

<br>
<img src="images/e05.PNG" width="600">
<br>
<img src="images/e06.PNG" width="600">
<br>

## - Final result

> 14. That's it. Now you have a fully functional **CentOS-Stream-9** VM in a **Windows 10** computer.

<br>
<img src="images/VBox52.PNG" width="800">
<br>

*Last updated: Antonio Mora, May 19th, 2022*
