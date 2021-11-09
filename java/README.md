<img src="https://github.com/mora-lab/mora-lab.github.io/blob/master/picture/MORALAB_Banner.png">

# Installing Java

**Java** is a high-level, multi-platform object-oriented programming language.<br><br>

## Java for windows:

### - Downloading:
> 1. Download Java from https://www.oracle.com/java/technologies/downloads/. For this tutorial, download **Java-11** from here: [jdk-11.0.11_windows-x64_bin.exe](https://www.oracle.com/java/technologies/downloads/#java11-windows). When you download Java, you will be asked to have an Oracle account and log in.
<br>

<img src="../neo4j/images/image-20210712155303913.png" alt="image-20210712155303913" style="zoom:50%;" />

### - Installing:

> 2. Click on `jdk-11.0.11_windows-x64_bin.exe` to install Java and follow the instructions.
<br>

<img src="../neo4j/images/image-20210712160717716.png" alt="image-20210712160717716" style="zoom:67%;" />

> **Note: You must remember the directory where you are installing Java, as we will use the path to set the environment variable for JAVA.**
<br>

<img src="../neo4j/images/image-20210712160834564.png" alt="image-20210712160834564" style="zoom:67%;" />
<img src="../neo4j/images/image-20210712165645433.png" alt="image-20210712165645433" style="zoom:67%;" />

### - Setting the environment variables for Java 11:

> 3. Go to `This PC` -> `Properties` -> `Advanced system settings` (alternatively, press `Win + R` and input `sysdm.cpl`).
<br>

<img src="../neo4j/images/image-20210712161608872.png" alt="image-20210712161608872" style="zoom:80%;" />

> 4. Go to the `Advanced` tab and click on `Environment Variables`.
<br>

<img src="../neo4j/images/image-20210712161741616.png" alt="image-20210712161741616" style="zoom:80%;" />

> 5. Click on `New...` to set a system variable for **JAVA 11**.
<br>

<img src="../neo4j/images/image-20210712165940834.png" alt="image-20210712165940834" style="zoom:67%;" />

> 6. Set `Variable name` as `JAVA_HOME11` and `Variable value` as the path of installing JAVA (the path of JAVA in my computer is `C:\Program Files\Java\jdk-11.0.13`).
<br>

<img src="../neo4j/images/image-20210712170101843.png" alt="image-20210712170101843" style="zoom:80%;" />

> 7. Now, click on `Path` in the list of `System variables` to add the JAVA variable. Then, click on `Edit...`.
<br>

<img src="../neo4j/images/image-20210712170146509.png" alt="image-20210712170146509" style="zoom:67%;" />

> 8. Click on `New` and write `%JAVA_HOME11%\bin`.
<br>

<img src="../neo4j/images/image-20210712170223572.png" alt="image-20210712170223572" style="zoom:80%;" />
<img src="../neo4j/images/image-20210712170420772.png" alt="image-20210712170420772" style="zoom:80%;" />
<img src="../neo4j/images/image-20210712170536796.png" alt="image-20210712170536796" style="zoom:80%;" />

### - Testing:

> 9. Type `cmd` on the Windows search box. Open the **CMD** (Windows Command Prompt), and write the command `java --version`.
<br>

![image-20210712171613788](../neo4j/images/image-20210712171613788.png)
<img src="../neo4j/images/image-20210714164012119.png" alt="image-20210714164012119" style="zoom:80%;" />

## Java for Linux CentOS:

> 11. To install java 11 on **CentOS**:
```
sudo yum install -y java-11-openjdk
sudo alternatives --config java
```

> 12. Choose the **java-11** option (the default might be an old `java-1.8` used by `libreoffice`).

> 13. Test the new version (now the default should be `java-11`).
```
java -version
```

*Last updated: Oct.30th, 2021*
