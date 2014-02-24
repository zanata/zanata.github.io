---
title: Downloading and Installing Zanata
layout: download
---

## Prerequisites

- JBoss Enterprise Application Platform 6 (EAP). This is the recommended container for Zanata, and it can be downloaded [here](http://www.jboss.org/jbossas/downloads/). You can also download a [pre-configured JBoss AS 7 here](http://sourceforge.net/projects/zanata/files/server/zanata-server.zip/download), but please note that this is not the supported configuration.
- A suitable MySQL database. This is NOT included in the Zanata archive. You can [download MySQL here](http://dev.mysql.com/downloads/mysql/).
- A database java connector (mysql-java-connector). This is included in the pre-configured JBoss AS from above, or it can be [downloaded here](http://dev.mysql.com/downloads/connector/j/).
- An email (SMTP) server to perform certain notifications.
- JDK version 6 or later.

The following packages are optional, but recommended:

- clamav for virus protection.
- Suitable fonts for CAPTCHA and server monitoring diagrams.

## Overview

Use the following steps to download and configure a Zanata server:

 1. Download and extract the server archive.
 1. Create a database for your Zanata data.
 1. Configure the admin users and email details.
 1. Start the server.

## Downloading and Extracting the Server Archive

Download and extract the [Zanata server archive](http://sourceforge.net/projects/zanata/files/server/zanata-server.zip/download):

In the following procedures, `<ZANATA DIR>` refers to the location where you extracted the Zanata server archive.

Alternatively, if you have downloaded EAP 6 for use with Zanata, please refer to the [following configuration guide](https://github.com/zanata/zanata-server/wiki/JBoss-AS-7) to fully configure your Zanata instance.

## Setting up the Zanata Database

 1. Download and install MySQL 5 from the [MySQL download page](http://dev.mysql.com/downloads/mysql/).
 Zanata has been thoroughly tested against MySQL 5 and the Zanata team therefore recommends that you install and use this version with Zanata.

 1. Create a database schema for Zanata. **NOTE:** Ensure that the default collation is UTF-8.

 ## Running the Zanata installer

Run the following commands on the terminal:

 1. `cd <ZANATA_DIR>/bin/zanata-installer`
 1. `./install.sh`  (for Windows there's `install.bat`)

The installer will ask some questions about the Zanata version you wish to install and the configuration of the Zanata database. After these have been answered, it will proceed to download the Zanata web application.

## Configuring Zanata

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

## Using Zanata

To start using your Zanata server, open a browser and navigate to `http://localhost:8080/zanata`

You can now upload some source strings and start translating. To get started, see [Adding Source Strings]({{ site.url }}/help/projects/add-source-strings).

<!---
<div class="txt--meta l--push-top-2">
<h3 class="epsilon">A few things to note:</h3>
<ul>
  <li>Zanata requires an email (SMTP) server to perform certain notifications.</li>
  <li>Make sure you are using JDK version 6 or higher.</li>
</ul>
</div>
--->