---
title:  "Podir Project Example"
last-updated: 2014-10-30
redirect_from: "/help/projects/podir-example/"
---

This document presents an example of a Zanata project with type `podir`. It assumes that you have already created a project and a version (See [Project Creation]({{ site.url }}/help/projects/create-version) ).

Podir projects consist of multiple source files (.pot) in a common source directory, and several translation files (.po) located in their corresponding locale's directory. Below is a typical directory structure for a Podir project:

```bash
project-name
|-- zanata.xml
|-- pot
|   |-- file1.pot
|   |-- file2.pot
|   |-- file3.pot
|-- ja
|   |-- file1.po
|   |-- file2.po
|   |-- file3.po
|-- es
|   |-- file1.po
|   |-- file2.po
|   |-- file3.po
|-- it
|   |-- file1.po
|   |-- file2.po
|   |-- file3.po
...
```

Notice the presence of the `zanta.xml` file already there. This file will be generated for you by the `{{ site.cli_client_name }} init` command, or you can download it from the Zanata server. For more information see [Configuring the Client]({{site.url}}/help/cli-configuration). This file will look something like this:

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<config xmlns="http://zanata.org/namespace/config/">
  <url>http://yourinstance.zanata.org/</url>
  <project>project-slug</project>
  <project-version>version-slug</project-version>
  <project-type>gettext</project-type>
  <locales>
    <locale>ja</locale>
    <locale>es</locale>
    <locale>it</locale>
    ...
  </locales>
</config>
```


### Pulling content from the server

To pull content from the server you should use the `{{ site.cli_client_name }} pull` command. Here are some of the commands you could use to pull content for this example project:

+ To pull translations only:

```bash
{{ site.cli_client_name }} pull -s pot -t .
```

+ To pull sources only

```bash
{{ site.cli_client_name }} pull -s pot -t . --pull-type source
```

+ To pull both sources and translations

```bash
{{ site.cli_client_name }} pull -s pot -t . --pull-type both
```


### Pushing content to the server

Similarly, the `{{ site.cli_client_name }} push` command is used to upload your content to the Zanata server. Here are some of the commands you might use for this example project:

+ To push translations only:

```bash
{{ site.cli_client_name }} push -s pot -t . --push-type trans
```

+ To push sources only

```bash
{{ site.cli_client_name }} push -s pot -t .
```

+ To push both sources and translations

```bash
{{ site.cli_client_name }} pull -s pot -t . --push-type both
```
