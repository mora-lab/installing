<img src="https://github.com/mora-lab/mora-lab.github.io/blob/master/picture/MORALAB_Banner.png">

# Installing Galaxy

> The following are the instructions to install Galaxy in a CentOS-Stream-8 OS. Installation in similar environments follows similar steps.

## - Pre-requisites

### If you are in Windows:
1. Create a Linux Virtual Machine. Follow the instructions here: [Creating a CentOS-8 VM](https://github.com/mora-lab/installing/tree/main/virtualbox).
2. Install Anaconda. Follow the instructions here: [Install Anaconda](https://github.com/mora-lab/installing/tree/main/anaconda).

### If you are in Linux:
1. Install Anaconda. Follow the instructions here: [Install Anaconda](https://github.com/mora-lab/installing/tree/main/anaconda).

### One more thing before starting...
Make sure that Anaconda's base environment is activated.
<br>
<br>
<img src="images/Galaxy01.PNG" width="600">
<br>

## - Install Galaxy using Git
<br>

> 1. Make a directory called "Galaxy".
```
mkdir Galaxy
```

<br>
<img src="images/Galaxy03.PNG" width="600">
<br>

> 2. Move to the folder you just created and install Git.
```
sudo yum install git
```

<br>
<img src="images/Galaxy05.PNG" width="600">
<br>

> 3. Get Galaxy using Git.
```
git clone -b release_21.01 https://github.com/galaxyproject/galaxy.git
```

<br>
<img src="images/Galaxy06.PNG" width="600">
<br>
<img src="images/Galaxy07.PNG" width="600">
<br>

## - Running Galaxy
<br>

> 4. Move to the *Galaxy/galaxy* directory and run the `run.sh` file.
<br>
<img src="images/Galaxy08.PNG" width="600">
<br>
<img src="images/Galaxy09.PNG" width="600">
<br>

> 5. Open a web browser at `localhost:8080`.
<br>
<img src="images/Galaxy10.PNG" width="600">
<br>

> 6. Close Galaxy (close web browser; Ctrl+C to the process in the terminal).

> 7. *Optional:* You can see that Galaxy has created its own python environment called `_ galaxy _`.
<br>
<img src="images/Galaxy11.PNG" width="600">
<br>

## - Create a Galaxy account
<br>

> 8. Again, go to *Galaxy/galaxy* and run the `run.sh` file.
<br>
<img src="images/Galaxy12.PNG" width="600">
<br>

> 9. Click on `Login or Register` and fill the information to open a new Galaxy account.
<br>
<img src="images/Galaxy13.PNG" width="600">
<br>

> 10. Restart Galaxy and you will find you will be logged in as your user name.
<br>
<img src="images/Galaxy14.PNG" width="600">
<br>

## - Changes to Galaxy configuration (Internet connection and Administrator account)
<br>

> 11. Go to the *Galaxy/galaxy* folder and make a copy of `galaxy.yml`:
```
cp config/galaxy.yml.sample config/galaxy.yml
```
<br>
<img src="images/Galaxy16.PNG" width="600">
<br>

> 12. Open the `galaxy.yml` file with a text editor:
```
vim config/galaxy.yml
```
<br>
<img src="images/Galaxy17.PNG" width="600">
<br>

> 13. Inside the vim editor, press `i` to edit (insert) new text. First, we will modify the address and port on which Galaxy will listen to the network (by default, only listens to localhost, ie., it is not accessible over the network). On line 24, change the default address to `0.0.0.0:8080`.
<br>
<img src="images/Galaxy18.PNG" width="600">
<br>

> 14. To save and leave **vim**, press *Esc* and then *:x*
<br>
<img src="images/Galaxy19.PNG" width="600">
<br>

> 15. Now we can add the `8080` port:
```
sudo firewall-cmd --zone=public --permanent --add-port=8080/tcp
sudo firewall-cmd --reload
```
<br>
<img src="images/Galaxy20.PNG" width="600">
<br>

> 16. Let's edit the configuration file again, now to add a Galaxy administrator:
```
vim config/galaxy.yml
```
<br>
<img src="images/Galaxy25.PNG" width="600">
<br>

> 17. Now we will change the field called `admin_users` by adding the username/email of the administrators. We can find it by pressing *Esc* and searching with `/.admin_users`. We can press `i`, go to line 1526, and directly add the username(s). Save and exit using `:x`.
<br>
<img src="images/Galaxy26.PNG" width="600">
<br>
<img src="images/Galaxy27.PNG" width="600">
<br>

> 18. Run Galaxy again and see the results. As you login with your username, an `Admin` menu has appeared. Clicking on that menu will show you all the administration options.
<br>
<img src="images/Galaxy28.PNG" width="600">
<br>
<img src="images/Galaxy30.PNG" width="600">
<br>

*Last updated: Antonio Mora, April 7th, 2021*
