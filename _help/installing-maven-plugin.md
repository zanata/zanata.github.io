---
title:  "Installing the Maven Plugin"
last-updated: 2014-10-30
redirect_from: "/help/maven-plugin/maven-plugin-install/"

pluginVersion: "3.1.2"
---

If your project uses Apache Maven, you can use Zanata's Maven Plugin rather than the command line client. The Maven Plugin can be used for non-Maven projects, but the same functionality is available in {{ site.cli_client_name }} without the need to install or configure Maven.

With Maven installed, the plugin can be run in the verbose form with no additional setup, or can be set up to use the concise form globally or for a single poject. The first time a command is run, the plugin and all its dependencies will be downloaded, which may take a while.

## Prerequisite - Install Maven

Zanata Maven plugin requires Apache Maven to be installed. Maven can be downloaded from [The Apache Maven website](http://maven.apache.org/) or installed using your operating system's package manager (e.g. `yum install maven`). Other installation options can be found at [Zanata wiki - Maven Plugin][wiki-zanata-plugin].

[wiki-zanata-plugin]: https://github.com/zanata/zanata-server/wiki/Zanata-Maven-Integration


## Verbose Command (No Additional Setup)

It is possible to run the Zanata plugin without any special setup once Maven is installed.

This is done by specifying the full plugin id including version on the command line. For example, the help command can be run with:

```bash
mvn org.zanata:zanata-maven-plugin:{{page.pluginVersion}}:help
```

The instructions in other sections will assume that you are using the concise form of the command, so if you choose to use the verbose form you should use `mvn org.zanata:zanata-maven-plugin:{{page.pluginVersion}}:` anywhere you see `mvn zanata:` in the instructions.

## Concise Command

Using global or per-project setup will allow the use of the concise form of the command, which would shorten the help command to:

```bash
mvn zanata:help
```

See "Global Command Configuration" under [Configuring the Maven Plugin]({{ site.url }}/help/maven-plugin/maven-plugin-config) for details.
