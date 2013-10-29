---
title: Downloading and Installing Zanata
layout: download
---

## Prerequisites

- Zanata requires an email (SMTP) server to perform certain notifications.
- Ensure you are using JDK version 6 or later.
- The Zanata server runs on JBoss Enterprise Application Platform (EAP). The Zanata archive contains a JBoss server with most of the configuration already complete. Any remaining configuration steps are described below.

## Overview

Use the following steps to download and configure a Zanata server:

 1. Download and extract the server archive.
 1. Create a database for your Zanata data.
 1. Configure the admin users and email details.
 1. Start the server.

## Downloading and Extracting the Server Archive

Download and extract the archive that best suits your needs:

- **Latest Release:** Click "Latest Release" to download the latest stable release. This is the easiest way to get Zanata up and running.

- **Earlier Releases:** For earlier releases, click "Earlier Releases," navigate to the required release, and download the archive.

In the following procedures, `<ZANATA DIR>` refers to the location where you extracted the Zanata archive.


## Setting up the Zanata Database

 1. Download and install MySQL 5 from the [MySQL download page](http://dev.mysql.com/downloads/mysql/).
 Zanata has been thoroughly tested against MySQL 5 and the Zanata team therefore recommends that you install and use this version with Zanata.

 1. Create a database schema for Zanata. **NOTE:** Ensure that the default collation is UTF-8.

 1. Configure Zanata to find this database.
 
 Open the `<ZANATA DIR>/standalone/deployments/zanata-ds.xml` file, which contains the database settings for Zanata.

 1. Modify the values for the following properties according to the database instance you have created for Zanata. If you are using MySQL as recommended, these are the only changes required.

- `connection-url` This is the database location. By default it is configured to localhost, port 3306, and a schema named `'zanata'`.
- `user-name` Database user name. This user name should have full table creation permissions on the database instance.
- `password` Database password.


## Configuring Zanata

Beginning with version 2.0, Zanata no longer creates an admin user by default. You need to register specific users to have administrative privileges.

 1. Open the `<ZANATA_SERVER>/standalone/configuration/standalone.xml` file.

 1. Locate the following line, and replace `"admin"` with a comma-separated list of users that require administrator privileges on the system.
 `<simple name="java:global/zanata/security/admin-users" value="admin"/>`

 1. Register a user under the name "admin", and it will automatically have administrator privileges. Any number of users may be added to this list in a comma-separated format.

 1. In the same file, configure other properties to your particular setup by adding more lines if necessary. The following properties must be configured in order for Zanata to run properly: 
 `java:global/zanata/email/default-from-address` 

 This is the default email address that will appear as sender on Zanata emails.

 1. The following properties relate to the SMTP email server that Zanata uses to send emails. It defaults to a locally installed server using port 25. If a particular property does not apply to the email server being used, it may be commented out or removed altogether.
 ```
java:global/zanata/smtp/host
java:global/zanata/smtp/port
java:global/zanata/smtp/username
java:global/zanata/smtp/password
java:global/zanata/smtp/tls
java:global/zanata/smtp/ssl
```


## Starting the Zanata Server

Run the following shell script to start the Zanata server:

```
<ZANATA DIR>/bin/start-zanata.sh
```

If you are running Microsoft Windows, run the following batch file:

```
<ZANATA DIR>/bin/start-zanata.bat
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