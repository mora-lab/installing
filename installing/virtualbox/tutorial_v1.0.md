![MoraLab](/picture/MORALAB_Banner.png)

# Installing Oracle VM VirtualBox

> The following are the instructions to install a virtual machine in Windows 10 (now referred as the "host" operative system). The chosen virtual machine is VirtualBox 6.1.18 and the system we will add "inside" the VM will be the CentOS-Stream-8 Linux system (now referred as the "guest" operative system), but a similar process can be followed for other host and guest OS.

## Downloads

> 1. Download VirtualBox from their website: [Download](https://download.virtualbox.org/virtualbox/6.1.18/VirtualBox-6.1.18-142142-Win.exe).

> 2. Download the ISO file with our guest OS (CentOS-Stream-8). You can find your favorite mirror site here: [Mirror sites](http://isoredirect.centos.org/centos/8-stream/isos/x86_64/). For this tutorial, we have downloaded our OS from here: [Download](http://download.nus.edu.sg/mirror/centos/8-stream/isos/x86_64/CentOS-Stream-8-x86_64-20210402-dvd1.iso).

## Installing VirtualBox

> 3. Run VirtualBox installation file. After running, you will receive a welcome message giving start to the installation process.

![MoraLab](images/VBox01.PNG | width=100)

> 4. Choose your desired location and other options.

![MoraLab](images/VBox02.PNG =250x250)
![MoraLab](images/VBox03.PNG | width=100)
![MoraLab](images/VBox04.PNG =250x250)
![MoraLab](images/VBox05.PNG | width=100)

> 5. After this, VirtualBox will be installed.

![MoraLab](images/VBox06.PNG)
![MoraLab](images/VBox07.PNG)

## Creating a new Virtual Machine

> 6. To create a new VM, click on "New" and choose a name, folder, and operative system to be installed.

![MoraLab](images/VBox11.PNG)

> 7. Define your desired memory and hard-disk specifications. Here we have chosen 8 GB memory and 40 GB hard disk.

![MoraLab](images/VBox12.PNG)
![MoraLab](images/VBox13.PNG)
![MoraLab](images/VBox14.PNG)
![MoraLab](images/VBox15.PNG)
![MoraLab](images/VBox16.PNG)

> 8. After this, your first Virtual Machine will be created.

![MoraLab](images/VBox17.PNG)

> 9. Optional: To improve the video memory, go to **Settings**, **Display**, and **Screen**. Here we raised the video memory from the specified value to 128 MB.

![MoraLab](images/VBox18.PNG)

## Installing CentOS-8

> 10. Now we can proceed to install the OS for our new VM. First, select the downloaded ISO file.

![MoraLab](images/VBox19.PNG)
![MoraLab](images/VBox20.PNG)
![MoraLab](images/VBox21.PNG)
![MoraLab](images/VBox22.PNG)

> 11. Press Start and the installation process will begin.

![MoraLab](images/VBox23.PNG)

> 12. Choose language and installation destination (hard disk). 

![MoraLab](images/VBox24.PNG)
![MoraLab](images/VBox25.PNG)
![MoraLab](images/VBox26.PNG)

> 13. Choose the base environment and additional software. We select a "Workstation" with GNOME, Internet, Office, and Development applications, but CentOS offers other possibilities such as servers and servers with GUI.

![MoraLab](images/VBox27.PNG)

> 14. Choose time/date and password, and you are ready to start installing CentOS.

![MoraLab](images/VBox28.PNG)
![MoraLab](images/VBox29.PNG)
![MoraLab](images/VBox30.PNG)

> 15. Press "Begin installation" and reboot after the process is finished.

![MoraLab](images/VBox32.PNG)

> 16. Accept the license agreement.

![MoraLab](images/VBox33.PNG)
![MoraLab](images/VBox34.PNG)
![MoraLab](images/VBox35.PNG)

> 17. Click on Finish configuration, and choose your privacy options.

![MoraLab](images/VBox37.PNG)

> 18. Finally, select your username and password.

![MoraLab](images/VBox38.PNG)
![MoraLab](images/VBox39.PNG)
![MoraLab](images/VBox40.PNG)

> 19. CentOS-8 is ready to be used inside the VirtualBox. However, you might find annoying that the resolution is low, the screen size stays small even if you maximize, and other details, so the next step is advised.

![MoraLab](images/VBox41.PNG)

## Installing CentOS-8 Guest Additions

> 20. Inside CentOS, go to **Devices**, **Insert Guest Additions CD image**, and follow the procedure.

![MoraLab](images/VBox47.PNG)
![MoraLab](images/VBox48.PNG)
![MoraLab](images/VBox49.PNG)
![MoraLab](images/VBox50.PNG)
![MoraLab](images/VBox51.PNG)

> 21. That's it. Now you have a fully functional CentOS-Stream-8 VM.

![MoraLab](images/VBox52.PNG)
