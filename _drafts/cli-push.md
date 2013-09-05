---
layout: help
title:  "Document Upload with Client"
categories:
- help
- cli
---

To upload documents to your project-version, the command-line client's `push` command can be used.

These instructions assume that you have installed {{ site.cli_client_name }} as shown in [Installing the Client]({{ site.url }}/help/cli/cli-install), and have saved user and project configuration as shown in [Configuring the Client][].

[Configuring the Client]: {{ site.url }}/help/cli/cli-configuration


## Source Document Upload

The basic command for uploading documents is `{{ site.cli_client_name }} push`. The push command should always be run from the directory that contains `zanata.xml` for your project (find information about `zanata.xml` at [Configuring the Client][]).

At the time of writing, you will have to specify source and translation directories with the command, even though the default push command will push only source documents to the server. This will be fixed in a future version. This means that the simplest push command is:

`{{ site.cli_client_name }} push -s src -t trans`

This command will:

 1. search for source documents in a directory named `src` and any of its subdirectories.
 1. display the current settings and list of source documents that were found.
 1. confirm that you want to proceed with the upload.
 1. upload the located source documents to the server.


For a full list of the available options for push, run `{{ site.cli_client_name }} help push`


## Translation Document Upload

The push command can also upload translations. This is mainly for use when translation has started on your project before it has moved to Zanata.

To push translations instead of source documents, add the option `--push-type trans`, like so:

```bash
{{ site.cli_client_name }} push --push-type trans -s src -t trans
```

To push source and translation documents together, use `--push-type both`.

*Note:* translation documents must be named appropriately to match a source document. The appropriate name depends on your project type. For example, if the above command is used for a Java Properties project with a source document `src/strings/messages.properties`, a Japanese translation for the document would be at `trans/strings/messages_ja.properties`.

```bash
src
  strings
    messages.properties
trans
  strings
    messages_ja.properties
```

If you are unsure about the layout and naming for translation files in the selected project type, you can do a trial pull and look at the output. This can be done by copying `zanata.xml` to an empty folder and running a pull command such as:

```bash
{{ site.cli_client_name }} pull -s src -t trans --create-skeletons
```

The option `--create-skeletons` is used to make sure files will be written even if there are no translations.

For more information on the pull command, see [Document Download with Client]({{ site.url }}/help/cli/cli-pull).
