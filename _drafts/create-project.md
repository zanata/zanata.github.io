---
layout: post
title:  "Project Creation"
categories:
- help
- projects
---

Anyone with an account can upload source strings to Zanata. The first step is to create a project:

 1. **Create a project.**
 1. [Create a version]({{ site.url }}/help/projects/create-version) under the project.
 1. Add documents to the version.
   - Using the website
   - Using the [command-line client push]({{ site.url }}/help/cli/cli-push) command

## Project creation through the website

To start creating a project on the Zanata website, click the `Create project` button on the `Projects` page, or use the `create your own` link on the user dashboard, at the bottom of the projects summary.

![Project creation button on Projects page]({{ site.url }}/images/302-projects-create-project.png)

Project creation button on `Projects` page.


![Shortcut project creation link on user dashboard]({{ site.url }}/images/302-user-dashboard-create-project.png)

Shortcut project creation link on user dashboard.


The following screenshot shows the project creation page. In the screenshot, all fields have been filled in to illustrate the process. This example would create a project with a URL ending in '/zanata-server', that will be displayed in the project list as 'Zanata Server'. Details for each of the fields are shown below.

![Example project creation form with all fields filled in]({{ site.url }}/images/302-create-project-completed.png)

------------


### Project ID

Project ID is a unique identifier for your project that will be used in the project's URL and in client configuration files. It should not contain any spaces.

### Name

Name is the display name for your project. Name is shown in all places that your project is shown, such as the project list, user dashboard and your project page. This should be a name that allows translators to easily recognize your project.

### Description

A short description to provide a little more information for translators to identify your project. Descripton is displayed in the project list.

### Project Type

Project Type defines the type of files that your project uses to store source and translation strings. This setting ensures that files for your project will be downloaded in the correct format.

There is a brief description for each project type. If the description is insufficient, more information on each project type is available at [Project Types wiki page](https://github.com/zanata/zanata/wiki/Project-Types).

### View source files

This is an optional field to provide a URL that translators can use to view the source files in their original format. This will be shown on your project's homepage as a clickable link. This will most commonly be a link to the source document in a version control system such as github. Providing this link can help professional translators provide high quality translations.

For example, the URL provided for the strings used in the Zanata user interface points to [Zanata Source Strings](https://github.com/zanata/zanata-server/blob/master/zanata-war/src/main/resources/messages.properties)

### Source Download/Checkout

This is an optional field to provide a machine-readable string that can be used to download the source files.

For example, a git checkout URL is provided for the Zanata server project that can be used with git command line to download a copy of the Zanata server source code as shown here:

```bash
$ git clone git@github.com:zanata/zanata-server.git
```

### Homepage Content

Homepage Content is optional rich text that will be shown on your project's home page. This can be used to provide more detailed information to translators to help them understand and translate your project.

### Status

Status is used to set a project to read-only, which prevents translations being entered. This may be useful in some cases, but should be used sparingly so that translators are able to work on your project.

### Customized locales

By default, your project will be available for translation to a set of locales defined on the Zanata server. If your project requires a different set of locales, check the 'Would you like to add a customized list of locales?' checkbox to see and modify a list of locales available for your project.

### Restrict access

The access restriction feature is intended for use with special roles that can be defined by an administrator. For example, the role 'Fedora_CLA' is automatically assigned by users who sign in using Fedora OpenID, and can be used here to ensure that Fedora translation is only performed by users who have accepted the Fedora Contributor License Agreement.

### Customized list of validations

Validations run in the translation editor and help translators to provide translations that are valid for your project. Any validations checked in this list will always be active in the translation editor. Other validations can be toggled by translators to suit their individual workflow.

At the time of writing, the recommended validations are recommended:

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


## Project creation from command line

Projects can also be created using the command-line client. See the help output of the client for a list of available options.