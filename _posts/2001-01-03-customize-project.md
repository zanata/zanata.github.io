---
layout: help
title:  "Project Settings"
categories:
- help
- projects
---

## Settings

Once a [project has been created]({{ site.url }}/help/projects/create-project), the maintainer can add further details and project behaviour via the Settings tab.
<figure>
<img alt="Project General Settings tab" src="{{ site.url }}/images/302-project-settings-button.png" />
<figcaption>Project Settings tab link.</figcaption>
</figure>

The Settings tab contains fields that manage appearance and workflow of your project.  Some of these are already covered in the [Project Creation]({{ site.url }}/help/projects/create-project) help.

------------

## General Settings

<figure>
<img alt="Project General Settings tab" src="{{ site.url }}/images/302-project-general-settings.png" />
<figcaption>Project General Settings tab</figcaption>
</figure>

### Project Type

Project Type defines the type of files that your project uses to store source and translation strings. This setting ensures that files for your project will be downloaded in the correct format.

There is a brief description for each project type. If the description is insufficient, more information on each project type is available at [Project Types wiki page](https://github.com/zanata/zanata/wiki/Project-Types).

### Home Page

This is an optional field to provide a URL that translators can use to view the source files in their original format. This will be shown on your project's homepage as a clickable link. This will most commonly be a link to the source document in a version control system such as github. Providing this link can help professional translators provide high quality translations.

For example, the URL provided for the strings used in the Zanata user interface points to [Zanata Source Strings](https://github.com/zanata/zanata-server/blob/master/zanata-war/src/main/resources/messages.properties)

### Repository

This is an optional field to provide a machine-readable string that can be used to download the source files.

For example, a git checkout URL is provided for the Zanata server project that can be used with git command line to download a copy of the Zanata server source code as shown here:

```bash
$ git clone git@github.com:zanata/zanata-server.git
```

### Make this project read only

This button is used to set a project to read-only, which prevents translations being entered. This may be useful in some cases, but should be used sparingly so that translators are able to work on your project.

This can be toggled using the same button, as desired.

------------

## Languages Settings

<figure>
<img alt="Project Languages Settings tab" src="{{ site.url }}/images/302-project-languages-settings.png" />
<figcaption>Project Languages Settings tab</figcaption>
</figure>

### Reset languages from global settings

By default, your project will be available for translation to a set of locales defined on the Zanata server. If your project has added or removed any languages, this button will appear, allowing you to reset the project's languages to the default list.

### The Languages list (and removing)

A list of languages supported by your project will appear here. Hovering on a language in this list will display an X which will remove that language from the list.

<figure>
<img alt="Removing a project language" src="{{ site.url }}/images/302-project-languages-remove.png" />
<figcaption>Removing a project language</figcaption>
</figure>

### Add a Language

Entering text into this field will search and filter Zanata's available languages and display them. Selecting a language from the drop-down will add it to the languages supported by your project.

<figure>
<img alt="Adding a project language" src="{{ site.url }}/images/302-project-languages-add.png" />
<figcaption>Adding a project language</figcaption>
</figure>

------------

## Translation Settings

<figure>
<img alt="Project Translation Settings tab" src="{{ site.url }}/images/302-project-translation-settings.png" />
<figcaption>Project Translation Settings tab</figcaption>
</figure>

### Validations

Validations run in the translation editor and help translators to provide translations that are valid for your project. Any validations checked in this list will always be active in the translation editor. Other validations can be toggled by translators to suit their individual workflow.

At the time of writing, the following validations are recommended:

 - all project types:
   - leading/trailing newline
   - tab characters
 - gettext/podir projects:
   - printf variables
   - positional printf
 - podir projects:
   - HTML/XML tags
 - java properties projects:
   - java variables
 - file projects with libreoffice documents:
   - HTML/XML tags

### Copy Translations settings

Copy Translations attempts to reuse translations that have been entered in Zanata by matching them with untranslated strings in your project/version.  These settings change the way Copy Translations behaves when a new version is created.

Refer to [the Copy Translations reference]({{ site.url }}/help/reuse/copytrans-explained) for more information.

------------

## Permissions Settings

<figure>
<img alt="Project Permissions Settings tab" src="{{ site.url }}/images/302-project-permissions-settings.png" />
<figcaption>Project Permissions Settings tab</figcaption>
</figure>

### Maintainers list

A list of maintainers for the project.  Hovering on a maintainer in this list will display an X which will remove that maintainer from the list.

### Add a Maintainer

Entering at least three characters of a username will search for and filter users by that entry.  Selecting an username will add that user to the list of maintainers for the project.

### Restrict access to certain user roles

The access restriction feature is intended for use with special roles that can be defined by an administrator. For example, the role 'Fedora_CLA' is automatically assigned by users who sign in using Fedora OpenID, and can be used here to ensure that Fedora translation is only performed by users who have accepted the Fedora Contributor License Agreement.

------------

## About

<figure>
<img alt="Project About Settings tab" src="{{ site.url }}/images/302-project-about-settings.png" />
<figcaption>Project About Settings tab</figcaption>
</figure>

About is optional rich text that will be shown on your project's about tab. This can be used to provide more detailed information to translators to help them understand and translate your project.
