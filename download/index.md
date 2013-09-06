---
title: Download
layout: download
---

## 1. Download

Download the package that best suits you:

**Zanata Server:** Easiest way to get Zanata up and running. Extract the contents of this file. The following steps will refer to this location as <ZANATA DIR>.

**Zanata Previous Releases:** For more experienced users. You will need to provide a JBoss installation, configure it, and deploy Zanata manually.

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

For more information, check out our [documentation](https://github.com/zanata/zanata-server/wiki/Developer-Guide).

<div class="txt--meta l--push-top-2">
<h3 class="epsilon">A few things to note:</h3>
<ul>
  <li>Zanata requires an email (SMTP) server to perform certain notifications.</li>
  <li>Make sure you are using JDK version 6 or higher.</li>
</ul>
</div>
