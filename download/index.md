---
title: Download
layout: download
---

Setting up a Zanata server takes a few simple steps:

 1. download and unzip the server package
 1. create a database for your Zanata data
 1. configure the admin user and email
 1. start up the server

## 1. Download

Download  and extract the package that best suits you:

**Latest Version:** Easiest way to get Zanata up and running.

**Previous Zanata Releases:** For older releases, use the "Previous Zanata Releases" link, navigate to the release number of interest and download the zip.

The following steps will refer to the extracted location as <ZANATA DIR>.


## 2. Setup the Zanata Database

Zanata has been thoroughly tested against MySQL 5 so it's recommended that you install and use it with Zanata. You can download a copy Here.

Once you have installed the Database server, create a database schema for Zanata (make sure the default collation is UTF-8).

Now you only need to tell Zanata where to find this database. To do this, open the file:

```
<ZANATA DIR>/server/zanata/deploy/zanata-ds.xml
```

This file contains the database settings for Zanata. Modify the values for the following properties according to the database instance you have created for zanata. (If you are using MySQL as recommended, you will only need to change these):

- `connection-url`: This is the database location. By default it is configured to localhost, port 3306 and a schema named `'zanata'`.
- `user-name`: Database user name. This user name should have full  table creation permissions on the database instance.
- `password`: Database password.


## 3. Configure Zanata

From version 2.0.x onwards, Zanata will no longer create an admin user by default. Instead, edit the file located at

```
<ZANATA_SERVER>/standalone/configuration/standalone.xml
```

By looking for the following line, and replacing the `'value'` by a list of users that should have administrator priviledges when joining the system.

```
<simple name="java:global/zanata/security/admin-users" value="admin"/>
```

Now register a user under the name "admin", and it will automatically have administrator privileges. Any number of users may be added to this list in a comma-separated format.

In the same file, configure other properties to your particular setup by adding more lines if necessary. The following properties should be configured in order for Zanata to run properly:

```
java:global/zanata/email/default-from-address
```

This is the default email address that will appear as sender on Zanata emails.

The following properties relate to the SMTP email server that Zanata uses to send emails. It defaults to a locally installed server using port 25. If a particular property does not apply to the email server being used, it may be commented out or removed altogether.

```
java:global/zanata/smtp/host
java:global/zanata/smtp/port
java:global/zanata/smtp/username
java:global/zanata/smtp/password
java:global/zanata/smtp/tls
java:global/zanata/smtp/ssl
```


## 4. Start Zanata

Starting zanata is as easy as running the 'start-zanata' executable found at

```
<ZANATA DIR>/bin/start-zanata.sh
```

... or for Windows users

```
<ZANATA DIR>/bin/start-zanata.bat
```


## 5. Start Using it!

Zanata should be available at

```
http://localhost:8080/zanata
```

You should now be able to upload some source strings and start translating. To get started, see [Adding Source Strings]({{ site.url }}/help/projects/add-source-strings).

<div class="txt--meta l--push-top-2">
<h3 class="epsilon">A few things to note:</h3>
<ul>
  <li>Zanata requires an email (SMTP) server to perform certain notifications.</li>
  <li>Make sure you are using JDK version 6 or higher.</li>
</ul>
</div>
