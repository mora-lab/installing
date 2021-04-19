<img src="https://github.com/mora-lab/mora-lab.github.io/blob/master/picture/MORALAB_Banner.png">

# Installing Planemo
<br>

> **Planemo** is a command-line utility "to assist in developing Galaxy and Common Workflow Language artifacts - including tools, workflows, and training materials". More information about **Planemo** can be found [here](https://).
> The following are the instructions to install **Planemo** (version 0.74.3) on Linux. The tutorial uses a **Linux CentOS-Stream-8** installed in a **VirtualBox 6.1.18** virtual machine. A similar procedure can be followed using other OS.

## - Before starting
<br>

> 1. In order to install Planemo, you must previously have installed **python**, **Galaxy** and **R/Rstudio** in a Linux environment.
If you don't have them installed yet, follow our tutorials:

[Creating a CentOS-Stream-8 VirtualBox VM](https://github.com/mora-lab/installing/blob/main/virtualbox/tutorial_v1.0.md)<br>
[Installing Anaconda](https://github.com/mora-lab/installing/blob/main/anaconda/tutorial_v1.0.md)<br>
[Installing Galaxy](https://github.com/mora-lab/installing/blob/main/galaxy/tutorial_v1.0.md)<br>
[Installing Rstudio](https://github.com/mora-lab/installing/blob/main/rstudio/tutorial_v1.0.md)<br>

> 2. Go to your Linux machine. In our case, open **VirtualBox** and start the VM. Open a terminal in your Linux environment.

## - Download and install
<br>

> 3. Download and install Planemo from conda.
```
conda config --add channels bioconda
conda config --add channels conda-forge
conda install planemo
```

<br>
<img src="images/Planem01.PNG" width="600">
<br>
<img src="images/Planem02.PNG" width="600">
<br>
<img src="images/Planem03.PNG" width="600">
<br>

> 4. Confirm the version of **Planemo** that you have installed (in our case, it is Planemo v0.74.3).

<br>
<img src="images/Planem04.PNG" width="600">
<br>

## Building an R test tool:

> 5. Open **Rstudio**.

<br>
<img src="images/Planem05.PNG" width="600">
<br>

> 6. Create an R script that inputs two parameters and passes them to the output.
```
#usage : Rscript r_test1.R <para1> <para2> <para3>

# parameters
args<-commandArgs(TRUE)
para1 <- args[1]
para2 <- args[2]
para3 <- args[3]

# R function
r_test <- function(para1 = para1, para2 = para2){
	x = paste0("parameter1 is:", para1, "; parameter2 is:", para2)
	return(x)
}

# example
x <- r_test(para1 = para1, para2 = para2)

# output
write.table(x, file = para3)
```

*commandArgs()* provides access to a copy of the command line arguments supplied when this R session vas invoked.

<br>
<img src="images/Planem07.PNG" width="600">
<br>

> 7. Save it as **test1.R** in a *test1* directory.

<br>
<img src="images/Planem08.PNG" width="600">
<br>

> 8. Open a terminal in **Rstudio** and run the **R** script.
```
cd Galaxy/test1/
Rscript test1.R 24 53 test1_result.txt
```

<br>
<img src="images/Planem09.PNG" width="600">
<br>

> 9. Verify that you obtained the result file.

<br>
<img src="images/Planem10.PNG" width="600">
<br>

> 10. You can also open the result file using **Rstudio**.

<br>
<img src="images/Planem11.PNG" width="600">
<br>

## Using Planemo to create the tool definition file:

> The Galaxy tool definition file is an XML file wrapping a tool written in another language. The XML file describes the user interface for the tool, how to invoke it, what options to pass, and what files it will produce as output. It does contain multiple tags and attributes. More information about the XML tool definition file can be found [here](https://).

> 11. Run the following command in a terminal to build a tool based on our **R** function.
```
planemo tool_init --force \
--id 'test1' \
--name 'Test R tool to pass parameters' \
--description 'Test R tool to pass parameters' \
--example_command 'Rscript test1.R 24 53 test1_result.txt' \
--example_input 24 \
--example_input 53 \
--example_output 'test1_result.txt' \
--requirement 'r-base@3.5.1' \
--test_case
```

<br>
<img src="images/Planem12.PNG" width="600">
<br>

> 12. Verify that the **test1.xml** file has been created. You can open this file in **Rstudio** to review its content.

<br>
<img src="images/Planem13.PNG" width="600">
<br>
<img src="images/Planem14.PNG" width="600">
<br>


> 13. Modify the *Rscript* command, the input arguments, and the help in the XML file, as described:
```
<tool id="test1" name="My first Galaxy tool" version="0.1.0" python_template_version
<description>Pass parameters to R and generate a text file with them</description
<requirements>
<requirement type="package" version="3.5.1">r-base</requirement>
</requirements>
<command detect_errors="exit_code"><![CDATA[
	Rscript $__tool_directory__/test1.R '$input1' '$input2' '$output1'
]]></command>
<inputs>
<param type="text" name="input1" value="" label="Label for the first parameter"
<param type="text" name="input2" value="" label="Label for the second parameter"
</inputs>
<outputs>
<data name="output1" format="txt" />
</outputs>
<tests>
<test>
<param name="input1" value="24"/>
<param name="input2" value="53"/>
<output name="output1" file="test1_result.txt"/>
</test>
</tests>
<help><![CDATA[
	#usage : Rscript test1.R <para1> <para2> <output_file>
	<para1> and <para2> are text
	<output_file> is a text file
]]></help>
</tool>
```

The following is a link to help us write attributes for all kinds of parameters: [Link](https://).

<br>
<img src="images/Planem15.PNG" width="600">
<br>

## - Update Galaxy:

> 14. Go to *Galaxy/galaxy/config* and create the file **tool_data_table_conf.xml** from the original **tool_data_table_conf.xml.sample**
```
cd config
cp tool_data_table_conf.xml.sample tool_data_table_conf.xml
ls tool_data*
```

<br>
<img src="images/Planem19.PNG" width="600">
<br>

## - Use Planemo to test the tool:


*Last updated: Antonio Mora, April 19th, 2021*
