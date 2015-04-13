---
title:  "Gettext Project Example"
last-updated: 2014-10-30
redirect_from: "/help/projects/gettext-example"
---

This document presents an example of a Zanata project with type `gettext`. It assumes that you have already created a project and a version (See [Project Creation]({{ site.url }}/help/projects/create-project) ).

Gettext projects consist of a single source file (.pot), and several translation files (.po) named after their corresponding locale. Below is a typical directory structure for a Gettext project:

```bash
project-name
|-- zanata.xml
|-- singlesourcefile.pot
|-- es_ES.po
|-- fr.po
|-- zh_TW.po
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
    <locale map-from="es_ES">es-ES</locale>
    <locale>fr</locale>
    <locale map-from="zh_TW">zh-Hant</locale>
    ...
  </locales>
</config>
```

This example is also using the locale mapping feature. The `map-from` attributes on the `locale` elements are telling the client that although it will find the files using locales `es_ES` and `zh_TW`, those translated documents should be stored in the server under locales `es-ES` and `zh-Hant`.

### Pulling content from the server

To pull content from the server you should use the `{{ site.cli_client_name }} pull` command. Here are some of the commands you could use to pull content for this example project:

+ To pull translations only:

```bash
{{ site.cli_client_name }} pull -s . -t .
```

+ To pull sources only

```bash
{{ site.cli_client_name }} pull -s . -t . --pull-type source
```

+ To pull both sources and translations

```bash
{{ site.cli_client_name }} pull -s . -t . --pull-type both
```


### Pushing content to the server

Similarly, the `{{ site.cli_client_name }} push` command is used to upload your content to the Zanata server. Here are some of the commands you might use for this example project:

+ To push translations only:

```bash
{{ site.cli_client_name }} push -s . -t . --push-type trans
```

+ To push sources only

```bash
{{ site.cli_client_name }} push -s . -t .
```

+ To push both sources and translations

```bash
{{ site.cli_client_name }} push -s . -t . --push-type both
```
