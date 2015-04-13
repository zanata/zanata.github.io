---
title:  "Maven Plugin Commands"
last-updated: 2014-10-30
redirect_from: "/help/maven-plugin/maven-plugin-commands"

pluginVersion: "3.1.2"
---

If your project uses Apache Maven, you can use Zanata's Maven Plugin rather than the command line client. The Maven Plugin can be used for non-Maven projects, but the same functionality is available in {{ site.cli_client_name }} without the need to install or configure Maven.

The following instructions assume that you have installed and configured the Zanata Maven Plugin. Instructions for installation and configuration are available at [Installing the Maven Plugin]({{ site.url }}/help/maven-plugin/maven-plugin-install) and [Configuring the Maven Plugin]({{ site.url }}/help/maven-plugin/maven-plugin-config)

## Basic Maven Plugin commands

Commands and options for the Maven Plugin are similar to commands and options for {{ site.cli_client_name }}, but with different syntax.

### Help

To see an overview of commands, use

```bash
mvn zanata:help
```

and for detailed help for a particular command, use something like

```
mvn zanata:help -Ddetail=true -Dgoal=push
```

These are equivalent to commands `{{ site.cli_client_name }} help` and `{{ site.cli_client_name }} help push` in {{ site.cli_client_name }}.

*Note:* an online view of the same help information can be viewed at [Maven Plugin Reference](https://zanata.ci.cloudbees.com/job/zanata-client-site/site/zanata-maven-plugin/plugin-info.html).

### Push

The basic push command is

```bash
mvn zanata:push
```

This will look for source documents in the location for `srcDir` specified in `pom.xml` and upload them to the server. If `srcDir` is not specified in `pom.xml`, the current directory will be used.

The source directory can be overridden on the command line as shown here:

```bash
mvn zanata:push -Dzanata.srcDir="src/messages"
```

This will look for source strings in "src/messages".

More detail on the push command can be found at [Document Upload with Client]({{ site.url }}/help/cli/cli-push)

### Pull

The basic pull command is

```bash
mvn zanata:pull
```

This will download translated documents from the server and save them in the location for `transDir` specified in `pom.xml`. If `transDir` is not specified in `pom.xml`, the current directory will be used.

To download the source documents as well, specify pull type 'both' as shown here:

```bash
mvn zanata:pull -Dzanata.pullType="both"
```

More detail on the pull command can be found at [Document Download with Client]({{ site.url }}/help/cli/cli-pull)
