---
layout: help
title:  "Configuring the Client"
categories:
- help
- cli
---

{{ site.cli_client_name }} requires User Configuration and Project-Version Configuration.

## User Configuration

User configuration stores your credentials so that {{ site.cli_client_name }} can prove to the server that requests are from you rather than an imposter. The information in your user config should be kept secret.

{{ site.cli_client_name }} expects to find user configuration in `.config/zanata.ini` within your user directory.

To add configuration for a Zanata server:

 1. Use your favourite text editor to create or open `zanata.ini` in `~/.config/`.
 1. Sign into the Zanata server and navigate to the user settings page
 1. Ensure that an API Key is shown. If you do not have an API Key, click 'Generate API Key' now.
![User settings page]({{ site.url }}/images/302-user-settings.png)

 1. Copy the contents of the text-box labeled 'Configuration [zanata.ini]'.
 1. Paste the copied lines into `zanata.ini` and save the file.


## Project-Version Configuration

Project configuration stores information about a project-version, and should be kept in the project directory.

{{ site.cli_client_name }} expects to find project-version configuration in a file named `zanata.xml` in the project directory.

To add project-version configuration to your project directory:

 1. Sign into the Zanata server and navigate to the appropriate version of your project.
 1. Click the `Config file` button to initiate download of `zanata.xml`.
![Config file button on version page]({{ site.url }}/images/302-version-config-file.png)

 1. Save `zanata.xml` in your project directory.


These steps should be repeated for each project-version before using any {{ site.cli_client_name }} commands for the project-version.

---

[Old instructions](https://github.com/zanata/zanata-server/wiki/Client-Configuration)
