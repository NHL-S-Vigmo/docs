# Installing the Vigmo Dashboard
In order to get the entire project up and running, we made this summary to get you through it.

## 1. Server Configuration
First you need to set up your hosting environment in the right way. We highly recommend you use linux. In the example we are using `Ubuntu 20.04.3 LTS`

### 1.1 Installing Everything
Before starting the commands make sure your system is up to date with 
```shell
sudo apt update
```
#### 1.1.1 Tomcat
Tomcat is a webserver used for running Java Web Application Runtimes (WAR)  
So before going further, make sure java is installed. Run this command to install: 
```shell
sudo apt install default-jdk
```
  1. Create a new tomcat user, since the server shouldn't run under the root user.
```shell
sudo useradd -r -m -U -d /opt/tomcat -s /bin/false tomcat
```
  2. Download the latest version of tomcat from their website [Download Tomcat 9](https://tomcat.apache.org/download-90.cgi)
```shell
wget http://www-eu.apache.org/dist/tomcat/tomcat-9/v9.0.27/bin/apache-tomcat-9.0.27.tar.gz -P /tmp
```

#### 1.1.2 MySQL

#### 1.1.3 NodeJS

#### 1.1.4 Ngnix

### 1.2 Database Configuration
Open up the mysql command prompt and sign in to begin this configuration step: 
`sudo mysql -u root` As the root user this should sign you in directly.

#### 1.2.1 Creating the database user.

#### 1.2.2 Creating vigmo database

Run the command `CREATE DATABASE vigmo;` to create the vigmo database. (if you prefer another name, you can replace this in every following script yourself)

Now run the latest database script found in the api repo (checking compatability with the latest release is recommended)
The script can be found [here /vigmo.sql](https://github.com/NHL-S-Vigmo/Api/blob/master/vigmo.sql)

#### 1.2.3 Granting the vigmo user permissions
In step [1.2.1](#1.2.1) we created the vigmo user on the database.

With this command you can grant him all privileges on the database created in step [1.2.2](#1.2.2)

```sql
GRANT ALL PRIVILEGES
```

### 1.3 
