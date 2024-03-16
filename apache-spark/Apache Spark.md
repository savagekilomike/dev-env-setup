https://spark.apache.org/downloads.html
https://www.oracle.com/java/technologies/downloads/

## Linux
**Udemy Course: Taming Big Data with Apache Spark and Python - Hands On!**
https://intellias.udemy.com/course/taming-big-data-with-apache-spark-hands-on/
https://www.sundog-education.com/spark-python/

Install Java, Scala, and Spark according to the particulars of your specific OS. A good starting point is [http://www.tutorialspoint.com/apache_spark/apache_spark_installation.ht](http://www.tutorialspoint.com/apache_spark/apache_spark_installation.htm)[m](http://www.tutorialspoint.com/apache_spark/apache_spark_installation.htm) [(](http://www.tutorialspoint.com/apache_spark/apache_spark_installation.htm)but be sure to install Spark 2.4.4 or newer)

### Step 1: Verifying Java Installation
Java installation is one of the mandatory things in installing Spark. Try the following command to verify the JAVA version.
```
$java -version 
```
If Java is already, installed on your system, you get to see the following response −
```
java version "1.7.0_71" 
Java(TM) SE Runtime Environment (build 1.7.0_71-b13) 
Java HotSpot(TM) Client VM (build 25.0-b02, mixed mode)
```
In case you do not have Java installed on your system, then Install Java before proceeding to next step.

### Step 2: Verifying Scala installation
You should Scala language to implement Spark. So let us verify Scala installation using following command.
```
$scala -version
```
If Scala is already installed on your system, you get to see the following response −
```
Scala code runner version 2.11.6 -- Copyright 2002-2013, LAMP/EPFL
```
In case you don’t have Scala installed on your system, then proceed to next step for Scala installation.

### Step 3: Downloading Scala
Download the latest version of Scala by visit the following link [Download Scala](http://www.scala-lang.org/download/). For this tutorial, we are using scala-2.11.6 version. After downloading, you will find the Scala tar file in the download folder.

### Step 4: Installing Scala
Follow the below given steps for installing Scala.
#### Extract the Scala tar file
Type the following command for extracting the Scala tar file.
```
$ tar xvf scala-2.11.6.tgz
```
#### Move Scala software files
Use the following commands for moving the Scala software files, to respective directory **(/usr/local/scala)**.
```
$ su – 
Password: 
cd /home/Hadoop/Downloads/ 
mv scala-2.11.6 /usr/local/scala 
exit 
```
#### Set PATH for Scala
Use the following command for setting PATH for Scala.
```
$ export PATH = $PATH:/usr/local/scala/bin
```
#### Verifying Scala Installation
After installation, it is better to verify it. Use the following command for verifying Scala installation.
```
$scala -version
```
If Scala is already installed on your system, you get to see the following response −
```
Scala code runner version 2.11.6 -- Copyright 2002-2013, LAMP/EPFL
```

### Step 5: Downloading Apache Spark
Download the latest version of Spark by visiting the following link [Download Spark](https://spark.apache.org/downloads.html). For this tutorial, we are using **spark-1.3.1-bin-hadoop2.6** version. After downloading it, you will find the Spark tar file in the download folder.

### Step 6: Installing Spark
Follow the steps given below for installing Spark.
https://spark.apache.org/downloads.html
#### Extracting Spark tar
The following command for extracting the spark tar file.
```
$ tar xvf spark-1.3.1-bin-hadoop2.6.tgz 
```
#### Moving Spark software files
The following commands for moving the Spark software files to respective directory **(/usr/local/spark)**.
```
$ su – 
Password:  

cd /home/Hadoop/Downloads/ 
mv spark-1.3.1-bin-hadoop2.6 /usr/local/spark 
exit 
```
#### Setting up the environment for Spark
Add the following line to ~**/.bashrc** file. It means adding the location, where the spark software file are located to the PATH variable.
```
export PATH=$PATH:/usr/local/spark/bin
```

Use the following command for sourcing the ~/.bashrc file.
```
$ source ~/.bashrc
```

### Step 7: Verifying the Spark Installation
Write the following command for opening Spark shell.
```
$spark-shell
```
If spark is installed successfully then you will find the following output.
```
Spark assembly has been built with Hive, including Datanucleus jars on classpath 
Using Spark's default log4j profile: org/apache/spark/log4j-defaults.properties 
15/06/04 15:25:22 INFO SecurityManager: Changing view acls to: hadoop 
15/06/04 15:25:22 INFO SecurityManager: Changing modify acls to: hadoop
15/06/04 15:25:22 INFO SecurityManager: SecurityManager: authentication disabled;
   ui acls disabled; users with view permissions: Set(hadoop); users with modify permissions: Set(hadoop) 
15/06/04 15:25:22 INFO HttpServer: Starting HTTP Server 
15/06/04 15:25:23 INFO Utils: Successfully started service 'HTTP class server' on port 43292. 
Welcome to 
      ____              __ 
     / __/__  ___ _____/ /__ 
    _\ \/ _ \/ _ `/ __/  '_/ 
   /___/ .__/\_,_/_/ /_/\_\   version 1.4.0 
      /_/  
		
Using Scala version 2.10.4 (Java HotSpot(TM) 64-Bit Server VM, Java 1.7.0_71) 
Type in expressions to have them evaluated. 
Spark context available as sc  
scala>
```

### **Anaconda for Python 3**
- Install the latest **Anaconda for Python 3** from anaconda.com


- Test it out!
    1. Open up a terminal
    2. cd into the directory you installed Spark, and do an ls to see what’s in there.
    3. Look for a text file we can play with, like README.md or CHANGES.txt
    4. Enter **pyspark**
    5. At this point you should have a >>> prompt. If not, double check the steps above.
    6. Enter **rdd = sc.textFile(“README.md”)** (or whatever text file you’ve found) Enter **rdd.count()**
    7. You should get a count of the number of lines in that file! Congratulations, you just ran your first Spark program!
    8. Enter quit() to exit the spark shell, and close the console window
    9. You’ve got everything set up! Hooray!


==непонятно в какой момент установился pyspark?==
или он сразу в комплекте шел?

```
venv / pipenv
pip install pyspark
```
