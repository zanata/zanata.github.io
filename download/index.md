---
title: Downloading and Installing Zanata
layout: download
---

## What you need

- JBoss Enterprise Application Platform 6.3 (EAP). This is the recommended container for Zanata, and it can be [downloaded here](http://www.jboss.org/jbossas/downloads/).
- ... OR Wildfly (recommended version is 8.1.x) which can be [downloaded here](http://wildfly.org/downloads/)
- A suitable MySQL database. This is NOT included in the Zanata archive. You can [download MySQL here](http://dev.mysql.com/downloads/mysql/).
- An email (SMTP) server to perform certain notifications.
- JDK version 7 or later (7 is recommended for EAP as it is not yet certified to run against Java 8). [OpenJDK](http://openjdk.java.net/install/) is recommended, but you can also download [Oracle's JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html)

The following packages are optional, but recommended:

- clamav for virus protection.

## Setting up the Zanata Database

 1. Download and install MySQL 5 from the [MySQL download page](http://dev.mysql.com/downloads/mysql/).
 Zanata has been thoroughly tested against MySQL 5 and the Zanata team therefore recommends that you install and use this version with Zanata.

 1. Create a database schema for Zanata. **NOTE:** Ensure that the default collation is UTF-8.

## Installing Zanata

You can run Zanata on JBoss EAP 6 or Wildfly. Just download one of the archives below for your platform, and then extract it on top of your JBoss or Wildfly installation.

- [Zanata for JBoss EAP](http://sourceforge.net/projects/zanata/files/server/zanata-server.zip/download)
- [Zanata for Wildfly](http://sourceforge.net/projects/zanata/files/server/zanata-server.zip/download)

## Run the installer

Zanata comes bundled with an installer that helps with some of the initial setup. Simply run `<ZANATA_SERVER>/bin/zanata-installer/install.sh` (there's also a .bat file if you are on Windows) and the installation sciprt will start asking some configuration questions.

The installer will also download the Zanata web application and place it in the JBoss installation.

## Some advanced configuration

Beginning with version 2.0, Zanata no longer creates an admin user by default. You need to register specific users to have administrative privileges.

 1. Open the `<ZANATA_SERVER>/standalone/configuration/standalone.xml` file.

 1. Locate the following line, and replace `admin` with a comma-separated list of users that require administrator privileges on the system.
 `<simple name="java:global/zanata/security/admin-users" value="admin"/>`

 1. Register a user under the name "admin", and it will automatically have administrator privileges. Any number of users may be added to this list in a comma-separated format.

 1. In the same file, configure other properties to your particular setup by adding more lines if necessary. The following properties must be configured in order for Zanata to run properly: 
 `<simple name="java:global/zanata/email/default-from-address" value="admin@example.com"/>` 

 This is the default email address that will appear as the sender on Zanata emails.

 1. The following properties relate to the SMTP email server that Zanata uses to send emails. It defaults to a locally installed server using port 25. Add suitable values to suit your configuration. If a particular property does not apply to the email server being used, you can comment it out or remove it completely.

  ```
  <simple name="java:global/zanata/smtp/host" value="" />
  <simple name="java:global/zanata/smtp/port" value="" />
  <simple name="java:global/zanata/smtp/username" value="" />
  <simple name="java:global/zanata/smtp/password" value="" />
  <simple name="java:global/zanata/smtp/tls" value="" />
  <simple name="java:global/zanata/smtp/ssl" value="" />
  ```

## Running Zanata

Go to the `<ZANATA_SERVER>/bin` directory and run the `standalone.sh` (Linux, Mac) or `standalone.bat` (Windows) file. 

## Using Zanata

To start using your Zanata server, open a browser and navigate to `http://localhost:8080/zanata`

You can now upload some source strings and start translating. To get started, see [Adding Source Strings]({{ site.url }}/help/projects/add-source-strings).
