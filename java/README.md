<img src="https://github.com/mora-lab/mora-lab.github.io/blob/master/picture/MORALAB_Banner.png">

# Java for windows
**Java** is...<br>

## - Download
> 1. Download Java [jdk-11.0.11_windows-x64_bin.exe](jdk-11.0.11_windows-x64_bin.exe) from https://www.oracle.com/java/technologies/javase-jdk11-downloads.html. When you download the Java file, you need to log in the Oracle.

<img src="images/image-20210712155303913.png" alt="image-20210712155303913" style="zoom:50%;" />

## - Install

> 2. **click [jdk-11.0.11_windows-x64_bin.exe](jdk-11.0.11_windows-x64_bin.exe) to install following its guide.**

<img src="images/image-20210712160717716.png" alt="image-20210712160717716" style="zoom:67%;" />

> **Note: You must remember where the directory to install Java, because we will use the path to set the environment variable for JAVA.**

<img src="images/image-20210712160834564.png" alt="image-20210712160834564" style="zoom:67%;" />

<img src="images/image-20210712165645433.png" alt="image-20210712165645433" style="zoom:67%;" />

## - Set the environment variable for Java 11

> 3. **Press `Win + R` to quickly launch apps, and input `sysdm.cpl` to open `System Properties`.**

<img src="images/image-20210712161608872.png" alt="image-20210712161608872" style="zoom:80%;" />

> 4. **Choose Advanced tab, and click the button `Environment Variables`.**

<img src="images/image-20210712161741616.png" alt="image-20210712161741616" style="zoom:80%;" />

> 5. **Click `New...` Button to set a system variables for JAVA 11.**

<img src="images/image-20210712165940834.png" alt="image-20210712165940834" style="zoom:67%;" />

> 6. **Set `Variable name` as `JAVA_HOME11` and `Variable value` as the path of installing JAVA (the path of JAVA in my computer is `C:\Program Files\Java\jdk-11.0.11`).**

<img src="images/image-20210712170101843.png" alt="image-20210712170101843" style="zoom:80%;" />

> 7. **Now, you should click the `Path` in the list of  `System variable` to add the JAVA variable. Then, click the button `Edit...`.**

<img src="images/image-20210712170146509.png" alt="image-20210712170146509" style="zoom:67%;" />

> 8. Click `New` Button to write `%JAVA_HOME11%\bin`.

<img src="images/image-20210712170223572.png" alt="image-20210712170223572" style="zoom:80%;" />

<img src="images/image-20210712170420772.png" alt="image-20210712170420772" style="zoom:80%;" />

<img src="images/image-20210712170536796.png" alt="image-20210712170536796" style="zoom:80%;" />

## - Test JAVA

> 9. **Open the CMD (Windows Command Prompt), and input the command `java --version` to test it.**

> 10. Press `Win + R` and input `cmd` to open CMD.

![image-20210712171613788](images/image-20210712171613788.png)

<img src="images/image-20210714164012119.png" alt="image-20210714164012119" style="zoom:80%;" />

# Java for Linux CentOS

> 11. To install java 11 on CentOS:

```
sudo yum install -y java-11-openjdk
sudo alternatives --config java
# Choose the java-11 option (the default might be an old java-1.8 used by libreoffice)
java -version # now the default should be java-11
```

*Last updated: Oct.30th, 2021*
