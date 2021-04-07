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
<br>
<img src="images/Galaxy03.PNG" width="600">
<br>

> 2. Move to the folder you just created and install Git.
<br>
<img src="images/Galaxy05.PNG" width="600">
<br>

> 3. Get Galaxy using Git.
<br>
<img src="images/Galaxy06.PNG" width="600">
<br>
<img src="images/Galaxy07.PNG" width="600">
<br>

## - Running Galaxy
<br>

> 4. Move to the *Galaxy/galaxy* directory and run the *run.sh* file.
<br>
<img src="images/Galaxy08.PNG" width="600">
<br>
<img src="images/Galaxy09.PNG" width="600">
<br>

> 5. Open a web browser at *localhost:8080*.
<br>
<img src="images/Galaxy10.PNG" width="600">
<br>

> 6. Close Galaxy (close web browser; Ctrl+C to the process in the terminal).

> 7. *Optional:* You can see that Galaxy has created its own pythin environment called *_galaxy_*.
<br>
<img src="images/Galaxy11.PNG" width="600">
<br>

## - Create a Galaxy account
<br>

> 8. Again, go to *Galaxy/galaxy* and run the *run.sh* file.
<br>
<img src="images/Galaxy12.PNG" width="600">
<br>

> 9. Click on *Login or Register* and fill the information to open a new Galaxy account.
<br>
<img src="images/Galaxy13.PNG" width="600">
<br>


*Last updated: Antonio Mora, April 7th, 2021*
