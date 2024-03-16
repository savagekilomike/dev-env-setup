# How to Check Java Version Installed on Linux
https://phoenixnap.com/kb/check-java-version-linux

## Method 1: Check the Java Version On Linux
To check the Java version on Linux Ubuntu/Debian/CentOS:
1. Open a terminal window.
2. Run the following command:
```bash
java -version
```
3. The output should display the version of the Java package installed on your system. In the example below, OpenJDK version 11 is installed.

You can also check the version of the primary Java compiler – javac (pronounced “java-see”) with the command:
```bash
javac -version   
```
## Method 2: Find Version by Checking Path Where Java is Installed
There are two ways to find the path of the Java directory.
The first option includes running a single command:
```bash
update-alternatives --list java
```
The system should respond with the path where Java is installed.

Alternatively, you can use the whereis command and follow the symbolic links to find the Java path.
1. Run the command:
```bash
whereis java
```
Check Java path on Ubuntu.
The output tells you that Java is located in /usr/bin/java.

2. List the content of the /usr/bin/java directory:
```bash
ls -l /usr/bin/java
```

Locate Java directory on Ubuntu.
Inspecting the directory shows that /usr/bin/java is only a symbolic link for /etc/alternatives/java.

3. Just like in the previous step, list the content of the provided path by running:
```bash
ls -l /etc/alternatives/java
```

Find Java path on Ubuntu.
Finally, the output displays /etc/alternatives/java is another symbolic link and that the real path of the Java directory is /usr/lib/jvm/java-11-openjdk-amd64/bin/java.

## Method 3: Search for Java in the Installed Packages List
You can also prompt the system to list installed packages and search for Java, with its version number.
Find Java by listing all installed packages.

1. To generate a list of all installed packages, use the command:
```bash
sudo apt list --installed
```

2. Scroll up/down until you find the Java packages as shown in this example.
Find Java in the installed packages list.
To avoid searching through all installed packages, list Java packages only. Prompt the system to list a specific software package. In this case, the package name is openjdk:
```bash
sudo apt list --installed | grep -i openjdk
```


# Installing OpenJDK 11 on Debian 12 Server or Desktop
https://linux.how2shout.com/installing-openjdk-11-on-debian-12-server-or-desktop/

## Carry out the system Update
```bash
sudo apt update
sudo apt upgrade
```

## Adding SID repository with preference
Well, OpenJDK 11 is not available through the default system repositories of Debian 12 instead version 17 is there. However, we can install OpenJDK 11 by adding the SID repository of Debian meant to install the latest packages for testing. Well, also to stop this repo from installing the latest untested packages automatically we will create a preference file.

First, edit the “sources.list” file and add the following line at the end of the file:
```bash
sudo nano /etc/apt/sources.list
```
At the end of the file add this line:
```bash
deb http://deb.debian.org/debian unstable main non-free contrib
```
Save the file by pressing Ctrl+O, hit the Enter key and Ctrl+X to exit

### Set preferences for the packages:
```bash
sudo nano /etc/apt/preferences
```
### Add the following lines, 
this will make our Debian 12 system only choose the stable packages while updating instead of unstable ones.
```bash
Package: *
Pin: release a=stable
Pin-Priority: 900

Package: *
Pin: release a=unstable
Pin-Priority: 50
```
Again save the file like we did earlier using Ctrl+O.

Run system update to refresh the APT repository cache:
```bash
sudo apt update
```

## Installing OpenJDK 11 Debian 12
Well, the OpenJDK 11 packages are available to install through the default repositories of almost all Linux distros. However, as we know in Debian 12 it is not available but after adding the SID repository we can get it like any other common package using the APT package manager. Here is the command to follow:
```bash
sudo apt install openjdk-11-jdk
```
Nevertheless, if you want to check out what other versions are available to install on your Debian 12 can use the given command.
```bash
sudo apt search openjdk
```
## Verifying the Installation
If you have completed the installation command to get OpenJDK 11 on Debian 12 then you would already have it, however, still, to confirm the same we can check the JAVA version using the given command.
```bash
java --version
```

## Set OpenJDK 11 as the default JAVA version
Now, we have the OpenJDK 11, but what if you already have OpenJDK 17 or any other version on your Debian 12 system, how will you make any one of them the system-wide default version?

Well, for that, we can use the **Update-alternatives** command to manage multiple versions of Java, if you have one.
```bash
sudo update-alternatives --config java
```
You will see the list of all Java versions installed on your Debian 12 system, now to set the one as the default enter the Selection number of that and hit the Enter key.

For example, we have JAVA 17 as the default version but we want that to be JAVA 11, so to do that will simply enter the selection number – 1 and press the Enter key.

Similarly, in the future, if we want to revert to Java 17 we run the Update-alternatives command again to select it.

## OpenJDK 11 Uninstallation (optional)
In the future, if you have completed your project and don’t need Java 11 anymore on your Debian 12 system then can remove it completely using the given command:
```bash
sudo apt remove openjdk-11*
```

## Frequently Asked Questions (FAQs)
1. How to switch between different Java versions installed on my Debian system? Switching between different Java versions is quite easy and can be achieved by using sudo update-alternatives --config java command. It will display a list of installed Java versions, we just need to enter the selection number of the corresponding version that we want to set default.
2. Is OpenJDK 11 suitable for use in enterprise-level applications and development? Yes, OpenJDK 11 is well-suited for enterprise-level applications. Its Long-Term Support (LTS) status ensures stability and ongoing updates, making it a reliable choice for businesses.
3. Can I install OpenJDK 11 alongside other Java versions?
Yes, we can install OpenJDK 11 alongside other Java versions. Debian to any other Linux will allow multiple Java installations and the good thing is we can switch between them using the update-alternatives command.
4. What is the key difference between OpenJDK 11 and Oracle JDK?
The primary difference is in licensing and support. OpenJDK 11 is open-source and free to use, while Oracle JDK may require a commercial license for certain uses. Both offer similar performance and features, but OpenJDK is generally preferred for open-source projects.

```bash
```

```bash
```

# How to set $JAVA_HOME





