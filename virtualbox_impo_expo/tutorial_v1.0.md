<img src="https://github.com/mora-lab/mora-lab.github.io/blob/master/picture/MORALAB_Banner.png">

# Importing and exporting virtual machines
<br>
> Instead of creating a new VM from scratch, as we learned [here](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v1.0.md), we might need to either import an existing virtual machine, with all its software and data, or export a virtual machine with all the software and data that we might have created. Two easy ways of doing that is by sharing a Virtual Disk Image (VDI) or an appliance (Open Virtualization format Archive, OVA).

## - Importing virtual disk images (VDI files):

> 1. Get your VDI file: You can find multiple VDIs on Internet (for example, at [OSBoxes](https://www.osboxes.org/virtualbox-images/), [Virtualboxes](https://virtualboxes.org/images/), or [VirtualDiskImages](http://virtualdiskimages.weebly.com/virtualbox.html)). For the purposes of this tutorial, download and unzip an image of [Lubuntu 20.04.1](https://sourceforge.net/projects/osboxes/files/v/vb/33-Lb--t/20.04.1/L20.04.1-VB-64bit.7z/download), which is a lightweight version of Ubuntu Linux.

> 2. Open **Virtual Box** and create a VM following the steps 1-7(a) of our [tutorial](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v1.0.md).
<br>
<img src="images/d01.PNG" width="600">
<br>
<img src="images/d02.PNG" width="600">
<br>

> 3. After you give a name to the VM and assign memory (and before assigning disk space and installing the OS), move the VDI file inside the new VM folder (the name you just assigned).

> 4. When you are in the "Create virtual machine/Hard disk" step, choose "Use an existing virtual hard disk file", click on the small folder, and find your VDI file.
<br>
<img src="images/d03.PNG" width="600">
<br>

> 5. Double-click and run the new VM.
<br>
<img src="images/d04.PNG" width="600">
<br>
<img src="images/d05.PNG" width="600">
<br>

> 6. Type the password and that's it. (Note: For all OSboxes' VDIs, username=osboxes, password=osboxes.org, root account password=osboxes.org).
<br>
<img src="images/d06.PNG" width="600">
<br>

## - Exporting virtual disk images (VDI files):

> 7. If you have already created a Virtual Machine (for example, after our [tutorial](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v1.0.md)), in order to share your disk, you just need to copy the VDI file to the new computer/location.

## - Importing appliances (OVA files):

> 8. First, get your OVA file. One example of OVA files that can be used in this tutorial is [PiRate](https://www.seanoe.org/data/00406/51795/data/53095.ova). Download the OVA file.

> 9. Open **Virtual Box**. In the *File* menu, select *Import Appliance* and then choose your OVA file.
<br>
<img src="images/e01.PNG" width="600">
<br>
<img src="images/e02.PNG" width="600">
<br>

> 10. You will get a box with the appliance settings. To avoid problems, uncheck all the controllers and update your base folder.
<br>
<img src="images/e03.PNG" width="600">
<br>
<img src="images/e03b.PNG" width="600">
<br>

> 11. Click on **Import**.
<br>
<img src="images/e04.PNG" width="600">
<br>

> 12. Double-click on your new VM.
<br>
<img src="images/e05.PNG" width="600">
<br>
<img src="images/e06.PNG" width="600">
<br>

## - Exporting appliances (OVA files):

> 13. In case you have already created a Virtual Machine (for example, in our [tutorial](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v1.0.md)), and you want to share it as an appliance, the procedure is equally simple. First, open **Virtual Box**. In the *File* menu, select *Export Appliance*. You will get a box to select the VM that you want to export.
<br>
<img src="images/f01.PNG" width="600">
<br>
<img src="images/f02.PNG" width="600">
<br>

> 14. You will get a box with some appliance settings. Choose the "Open Virtualization Format", together with the desired location and name of your new OVA file.
<br>
<img src="images/f03.PNG" width="600">
<br>

> 15. Then you will get the option to add some descriptive information to the virtual appliance (Optional).
<br>
<img src="images/f04.PNG" width="600">
<br>
<img src="images/f05.PNG" width="600">
<br>

> 16. Press **Export** and the OVA file will be generated in the specified location.
<br>
<img src="images/f06.PNG" width="600">
<br>

*Last updated: May 14th, 2021*
