# How to Install Java on Debian 12?
https://linuxgenie.net/how-to-install-java-on-debian-12/

Java is a free-to-use programming language used widely in web, android, and desktop application development and game development. Java is an Object-Oriented Language that supports technologies like virtual reality, machine learning, and multi-threading.

Java environment is easy to configure and manage across various platforms, including Debian (and other Linux distributions). The compatibility of Java with Debian is verified and thus a large community of Java developers are using it on Debian.

This article will demonstrate the installation and setting up of Java on Debian 12 (Bookworm) systems, with the following outline:
- How to Install Java on Debian 12?
- How to Configure Environment Variables on Debian 12?
- How to Run Java Scripts on Debian 12?
- How to Uninstall/Remove Java on Debian 12?

Let’s begin by discussing the installation of Java on Debian 12.

## How to Install Java on Debian 12?
There are multiple methods to install Java on Debian 12 systems which are demonstrated below:

## Method 1: How to Install Java via APT Packet Manager on Debian 12?
The Advanced Package Tool (APT) is the main command-line package management tool for Debian systems. To install Java via the APT packet manager, follow the below-mentioned steps:

### Step 1: Update System Repositories
Update the packages list to load any latest version by the following command:
```bash
sudo apt update
```

### Step 2: Install Java
To install the latest version of JDK available on the APT repository, i.e., JDK 17 (at the time of writing this article), run the following command:
```bash
sudo apt install default-jdk
```
The above output indicates that JDK 17 has been installed successfully.

### Step 3: Verify Java Installation
Check the version of Java by executing the following command:
```bash
java –version
```

## Method 2: How to Install Java via the Debian Package?
A Debian Package is a compressed archive used by Debian. A Debian package contains binary packages and source packages. To install Java via the Debian Package, follow the below-mentioned steps:

### Step 1: Update System Repositories
To ensure that the system repositories are up to date, run the following command:
```bash
sudo apt update
```

The above output displays that all existing packages are up to date.

### Step 2: Download the Debian Package of JDK 21
The Debian package of JDK is available for download on the Oracle’s official website. To download the Debian Package containing the latest version of JDK, execute the following command:
```bash
wget https://download.oracle.com/java/21/latest/jdk-21_linux-x64_bin.deb
```

Here’s the link to download the Debian package containing JDK 21.


### Step 3: Install Java
To install the Debian package, jdk-21_linux-x64_bin.deb containing JDK 21, execute the below-mentioned command:
```bash
sudo dpkg -i jdk-21_linux-x64_bin.deb
```

### Step 4: Verify Java Installation
Use the command below to verify Java’s version:
```bash
java –version
```

## Method 3: How to Install Java via Compressed Archive on Debian 12?
Software packages are typically available to download from the internet in compressed archives. There are many types of compressed archives among which, tar.gz is a popular compressed archive format. To install Java via Compressed Archive Package:

### Step 1: Update System Repositories
Execute the following command to ensure that the system repositories are up to date:
```bash
sudo apt update
```
### Step 2: Download the Compressed Archive of JDK 21
The tar.gz compressed archive of JDK is available for download on Oracle’s official website. To download the compressed archive containing the latest version of JDK execute the following command:
```bash
wget https://download.oracle.com/java/21/latest/jdk-21_linux-x64_bin.tar.gz
```
Find the link to download that tar.gz compressed archive containing JDK 21.

### Step 3: Extract the JDK 21 Compressed Archive
Create a new directory “java” to extract jdk-21_linux-x64_bin.tar.gz via the mkdir command:
```bash
sudo mkdir /usr/java
```

Next, extract the jdk-21_linux-x64_bin.tar.gz in the newly created directory “java” by executing the following command:
```bash
sudo tar -xzvf jdk-21_linux-x64_bin.tar.gz -C /usr/java
```

The error-free execution of the above command indicates the successful extraction of the archive: jdk-21_linux-x64_bin.tar.gz.

Next, configure the environment variables as shown in How to Configure Environment Variables on Debian 12. Otherwise, you won’t be able to locate the Java executable(s) in your system.

## How to Configure Environment Variables on Debian 12?
After the JDK is installed, the next step is configuring the environment variables JAVA_HOME and PATH to guarantee the proper execution of Java applications (without stating the path). The environment variables: JAVA_HOME and PATH are configured by adding the JDK to the path of Debian 12.

### Step 1: Find the Directory where JDK has been Installed
To find the directory where the JDK has been installed, execute the following command:
```bash
ls -d /usr/lib/jvm/jdk*
```

The above output shows the path of the directory where JDK 21 is installed, i.e., “/usr/lib/jvm/jdk-21-oracle-x64”.

In case the installation via tar.gz compressed archive, find the directory by entering the path of the file created in this step in the following command:
```bash
ls -d <path/jdk*>
```

### Step 2: Adding JDK 21 Directory to the Path of Debian 12
To add the JDK directory to the path of Debian 12, edit the .bashrc (startup file). Launch the .bashrc file in any text editor, for example, nano text editor by funning the command below:
```bash
nano .bashrc
```

Next, type the following script in the file .bashrc file:
```bash
export JAVA_HOME=”/usr/java/jdk-21.0.1″
export PATH=”$PATH:${JAVA_HOME}/bin”
```

Where the JAVA_HOME variable is utilized by many applications to find Java binaries and libraries.

Next, restart the terminal for the changes to take effect.

Step 3: Verify the Environment Variables Configuration
To verify if the JAVA_HOME variable is correctly configured and if Debian’s PATH environment variable contains the JDK 21 directory, execute the following commands:
```bash
echo $JAVA_HOME
echo $PATH
```
The above output verifies that the $JAVA_HOME variable is configured and the $PATH environment variable of Debian 12 contains the JDK 21 directory.

How to Run Java Scripts on Debian 12?
To create a new Java script “welcome.java”, first, launch a text editor, for example, nano text editor as shown below:
```bash
nano welcome.java
```

Type a basic Java script to print “Welcome to Linux Genie!” in the text editor as shown below:
```bash
class LinuxGenie {
  public static void main(String args[])
  {
    System.out.println(“Welcome to LinuxGenie!”);
  }
}
```

To compile the Java script by javac compiler, execute the following command:
```bash
javac welcome.java
```

Next, run the Java script by the following command:
```bash
java welcome.java
```


The above script returns the expected output, i.e., “Welcome to Linux Genie!” which indicates that the script is executed successfully.

## How to Uninstall/Remove Java on Debian 12?
Java can be uninstalled on Debian 12 by the following methods:

### Method 1: How to Uninstall Java via APT Packet Manager on Debian 12?
To uninstall Java via the apt package manager, run the following command:
```bash
sudo apt purge default-jdk
```
Where “purge” removes everything related to the JDK file: default-jdk.

### Method 2: How to Un-Install Java via DPKG Packet Manager on Debian 12?
To uninstall Java via the dpkg package manager, run the following command:
```bash
sudo dpkg -r jdk-<package-version>
```
Note: The JDK package version can be determined by running the “java –version” command.

To verify Java’s uninstallation, run the below-mentioned command:
```bash
java –version
```
### Method 3: How to Un-Install Java by Removing Java-Related Directories on Debian 12?
To uninstall Java by removing all Java-related directories, execute the following command:
```bash
sudo rm -rf <path/of/directory>
```
Where “f” searches for the files and “r” recursively deletes the directory containing java-related files (/usr/lib/jvm/* in this case).

Java’s installation can be verified by the command below:
```bash
java –version
```

Note: In case the JDK is installed via the Debian package or compressed archive, delete these packages to conserve disk space by running the following command:
```bash
rm <package>
```

## Conclusion
There are several methods to install Java on Debian 12 systems: 
installation via default apt repository and by downloading the Debian package and .tar.gz compressed archive. 
To install the latest version of JDK available on the apt repository, execute the 
```bash
sudo apt install default-jdk
```

To verify java’s installation, run the “java –version“ command. 
This article demonstrated three different methods of installing Java along with setting up environment variables on Debian 12 (Bookworm) systems.
