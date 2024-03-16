# Install PostgreSQL

https://www.postgresqltutorial.com/postgresql-getting-started/install-postgresql-linux/


## Самая адекватная инсталляция
https://www.howtoforge.com/how-to-install-postgresql-and-pgadmin-tool-on-debian-12/

https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-22-04

```bash
sudo apt update
sudo apt install postgresql postgresql-contrib
```

## Run pg - optinal, is started after installation by default
```bash
sudo systemctl start postgresql.service
```

## Secure your PostgreSQL Database
```bash
sudo -u postgres psql
```

```postgresql
postgres=# ALTER USER postgres PASSWORD 'DBStr0ngUserPassw0rd';
ALTER ROLE
postgres=#

postgres=# \q
```


## Start, Stop, Status
**check the version of your PostgreSQL**
```bash
sudo -u postgres psql -c "SELECT version();"
```

**status**
```bash
sudo systemctl status postgresql
```

**start**
```bash
sudo systemctl start postgresql
```

**restart**
```bash
sudo systemctl restart postgresql
```

**reload**
```bash
sudo systemctl reload postgresql
```

**stop**
```bash
sudo systemctl stop postgresql
```

## Set PostgreSQL to start automatically on system startup
```bash
sudo systemctl enable postgresql --now
```

https://www.linuxcapable.com/how-to-install-postgresql-15-on-debian-linux/
**Interacting with the PostgreSQL Account**
```bash
sudo -i -u postgres
PostgreSQL
exit
```


**Do some work in psql**
```bash
sudo -u postgres psql -d [db name]```


**Change the Ownership (Optional):**
```bash
sudo chown postgres:postgres /path/to/your/file.csv
```

**Assign Read Permissions**
```bash
sudo chmod +r /path/to/your/file.csv
```

**Restart PostgreSQL**
```bash
sudo service postgresql restart
```


## UNINSTALL
**To uninstall only the postgresql package:**
```bash
$ sudo apt purge postgresql postgresql-contrib -y
sudo apt-get remove postgresql
```

**Uninstall postgresql And Its Dependencies**
```bash
sudo apt-get -y autoremove postgresql
```


**Remove postgresql Configurations and Data**
```bash
sudo apt-get -y purge postgresql
```

**Remove postgresql configuration, data, and all of its dependencies**
```bash
sudo apt-get -y autoremove --purge postgresql
```
