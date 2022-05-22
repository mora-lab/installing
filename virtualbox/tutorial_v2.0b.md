<img src="https://github.com/mora-lab/mora-lab.github.io/blob/master/picture/MORALAB_Banner.png">

# Creating a new Virtual Machine using VirtualBox
<br>

> The following are the instructions to create a virtual machine (VM) in **VirtualBox 6.1.34** for **Windows 10** (now referred as the "host" operative system) and install **Mint-20.3-xfce** Linux system (now referred as the "guest" operative system). A similar process can be followed for other host and guest OS.

## - Downloads
<br>

> 1. Download the ISO file with our guest OS (Mint-20.3-xfce) [here](https://linuxmint.com/edition.php?id=294). For this tutorial, we have downloaded our OS from here: [Download](https://mirrors.layeronline.com/linuxmint/stable/20.3/linuxmint-20.3-xfce-64bit.iso).

## - Installing VirtualBox
<br>

> 2. If you haven't installed **VirtualBox**, first go to our tutorial to install it:

> [How to install VirtualBox](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v2.0a.md)

## - Creating a new Virtual Machine
<br>

> 3. Open **VirtualBox**. To create a new VM, click on **"New"** and choose a name, folder, and operative system to be installed.

<br>
<img src="images/VBox69.PNG" width="400">
<br>

> 4. Define your desired memory and hard-disk specifications. Here we have chosen 8 GB memory and 80 GB hard disk.

<br>
<img src="images/VBox70.PNG" width="400">
<br>
<img src="images/VBox71.PNG" width="400">
<br>
<img src="images/VBox72.PNG" width="400">
<br>
<img src="images/VBox73.PNG" width="400">
<br>
<img src="images/VBox74.PNG" width="400">
<br>

> 5. After this, your first Virtual Machine will be created.

<br>
<img src="images/VBox84.PNG" width="500">
<br>

> 6. Optional: To improve the video memory, go to **Settings**, **Display**, and **Screen**. Here we raised the video memory from the specified value to 128 MB.

<br>
<img src="images/VBox75.PNG" width="500">
<br>

> 7. Optional: Go to *Settings - USB*, press the right side icon, and find the device you want to mount.

<br>
<img src="images/VBox76.PNG" width="600">
<br>
<img src="images/VBox77.PNG" width="600">
<br>
<img src="images/VBox78.PNG" width="600">
<br>

## - Installing the OS in our VM (Mint-20.3-xfce)
<br>

> 8. Now we can proceed to install the OS for our new VM: First, click on the new VM and the "Select startup disk" window will be opened. Then click on the small folder icon to get the "Optical disk selector" window, click on "Add" and find the ISO file of our OS that you previously downloaded, and, finally, select the downloaded ISO file and click on "Create".

<br>
<img src="images/VBox79.PNG" width="400">
<br>
<img src="images/VBox80.PNG" width="400">
<br>
<img src="images/VBox81.PNG" width="400">
<br>
<img src="images/VBox82.PNG" width="400">
<br>

> 9. Press **Start** and the installation process will begin.

<br>
<img src="images/VBox83.PNG" width="400">
<br>

> 10. Click on "Install Linux Mint".

<br>
<img src="images/VBox85.PNG" width="400">
<br>

> 11. Select installation language and keyboard layout. 

<br>
<img src="images/VBox86.PNG" width="400">
<br>
<img src="images/VBox87.PNG" width="400">
<br>

> 12. Select installation type options, including multimedia codecs and erase disk options.

<br>
<img src="images/VBox88.PNG" width="400">
<br>
<img src="images/VBox89.PNG" width="400">
<br>
<img src="images/VBox90.PNG" width="400">
<br>
<img src="images/VBox91.PNG" width="400">
<br>

> 13. Choose location, username, and password.

<br>
<img src="images/VBox92.PNG" width="400">
<br>
<img src="images/VBox93.PNG" width="400">
<br>

> 14. Linux Mint will then be installed. After installation is finished, you will be prompted to press **Restart Now** and **Enter**.

<br>
<img src="images/VBox94.PNG" width="400">
<br>
<img src="images/VBox95.PNG" width="400">
<br>
<img src="images/VBox96.PNG" width="400">
<br>

> 15. Type your password and you should gain access to Linux Mint.

<br>
<img src="images/VBox97.PNG" width="400">
<br>
<img src="images/VBox98.PNG" width="400">
<br>

> 16. If the **Update Manager** icon displays a red spot, you may need to click to update some of the software.

<br>
<img src="images/VBox99.PNG" width="400">
<br>
<img src="images/VBox99b.PNG" width="400">
<br>

> 17. As an alternative, we can use **apt update** and **apt upgrade**.

<br>
<img src="images/VBox100.PNG" width="400">
<br>
<img src="images/VBox101.PNG" width="400">
<br>

> 18. Linux Mint is ready to be used inside the VirtualBox. However, you might find annoying that the resolution is low, the screen size stays small even if you maximize, and other details, so the next step is advised.

## - Installing VirtualBox Guest Additions
<br>

> 19. Open a terminal and follow the procedure.

<br>
<img src="images/VBox102.PNG" width="400">
<br>
<img src="images/VBox103.PNG" width="400">
<br>

> 20. In the VM menu, go to **Devices** and click on **Insert Guest Additions CD image**.

<br>
<img src="images/VBox104.PNG" width="400">
<br>
<img src="images/VBox105.PNG" width="400">
<br>

> 21. If the CD image runs automatically, simply follow the steps. If not, open a terminal and run it as in the following example.

<br>
<img src="images/VBox106.PNG" width="400">
<br>
<img src="images/VBox107.PNG" width="400">
<br>

> 22. Restart the VM.

<br>
<img src="images/VBox108.PNG" width="400">
<br>

> 23. After restarting, you can immediately observe the changes in the screen.

<br>
<img src="images/VBox109.PNG" width="500">
<br>

## - Using the USB drive

> 24. To mount the USB drive, go to the menu and click on **Devices** -> **USB** -> and then the name of your USB device.

<br>
<img src="images/VBox110.PNG" width="500">
<br>

> 25. You can now open the file manager and see the USB (in our case, appears as a "32 GB volume").

<br>
<img src="images/VBox111.PNG" width="500">
<br>

## - Final result

> 26. That's it. Now you have a fully functional **Mint-20.3-xfce** VM in a **Windows 10** computer.

<br>
<img src="images/VBox109.PNG" width="600">
<br>

## - Troubleshooting

> Problem1. When you maximize your VM, only the VM menu maximizes while the Linux Mint windows stays small.
Solution1. You just need to minimize and maximize again and the changes will be evident.

> Problem2. When installing the Guest Additions, you get the error message "VERR_PDM_MEDIA_LOCKED".
Solution2. You might need to close the VM, go to **Settings**/**Storage**, click on the CD icon, and click on **Leave empty**. Then return to the VM and try to install again.

<br>
<img src="images/Tr1.PNG" width="600">
<br>

*Last updated: Antonio Mora, May 22nd, 2022*
