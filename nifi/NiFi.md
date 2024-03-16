
```bash
# The following command can be used to change the username and password:
$ ./bin/nifi.sh set-single-user-credentials <username> <password>

# View current user/password
$ grep Generated logs/nifi-app*log
```

https://nifi.apache.org/download.html
1. **By using curl, you can download NiFi using the following command line:**
```bash
curl https://mirrors.estointernet.in/apache/nifi/1.12.1/nifi-1.12.1-bin.tar.gz
```

2. **Extract the NiFi files from the .tar.gz file using the following command:**
```bash
tar xvzf nifi.tar.gz
```

3. **You will now have a folder named nifi-1.12.1. You can run NiFi by executing the following from inside the folder:**
```bash
bin/nifi.sh start
```


```bash
vn@Ununtu-20:/opt/nifi$ grep Generated logs/nifi-app*log
Username [7a6efbb6-a225-4195-9e83-3ea8fa76431b]
Password [iuwktMyiaFgqNG6suWjyKCRzA7S+TajV]
```


4. **If you already have Java installed and configured, when you run the status tool as**
**shown in the following snippet, you will see a path set for JAVA_HOME**:
```bash
sudo bin/nifi.sh status
```

5. **If you do not see JAVA_HOME set, you may need to install Java using the following**
**command:**
```bash
sudo apt install openjdk-11-jre-headless
```

6. **Then, you should edit .bash_profile to include the following line so that NiFi**
**can find the JAVA_HOME variable:**
```bash
export JAVA_HOME=/usr/lib/jvm/java11-openjdk-amd64
```

7. **Lastly, reload .bash_profile:**
```bash
source .bash_profile
```

8. **When you run for the status on NiFi, you should now see a path for JAVA_HOME:**
```bash
sudo nifi*/bin/nifi.sh start
```

9. **When NiFi is ready, which may take a minute, open your web browser and go to**
**http://localhost:8080/nifi/. You should be seeing the following screen:**

In conf/nifi.properties, change nifi.web.http.port=8080 under the web properties heading to 9300, as shown:

**\# web properties #**
```bash
nifi.web.http.port=9300
```

**If your firewall is on, you may need to open the port:**
```bash
sudo ufw allow 9300/tcp
```

Now, you can relaunch NiFi and view the GUI at http://localhost:9300/nifi/.