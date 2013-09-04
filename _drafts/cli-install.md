---
layout: post
title:  "Installing the Client"
categories:
- help
- cli
---

The Zanata client ({{ site.cli_client_name }}) can be installed on most systems. Installation is easiest under Fedora, other systems can use Apache Ivy for installation. Manual installation is also possible.

## {{ site.cli_client_name }} Installation on Fedora

If you are using Fedora, {{ site.cli_client_name }} is available through the `yum` package manager.

```bash
sudo yum install zanata-client
```

## {{ site.cli_client_name }} Installation with Ivy

The Ivy distribution of the client is a small script that will download the client the first time it is run. This distribution requires Apache Ivy to run.

Instructions for installing Apache Ivy and the Ivy version of {{ site.cli_client_name }} can be found at [Zanata Ivy Client on github](https://github.com/zanata/zanata-client-ivy).

*Note:* The Ivy client will download required files the first time it is run, which may take several minutes. It will show `resolving dependencies...` while this is happening.

## {{ site.cli_client_name }} Nightly Builds

If you like to live dangerously, the client nightly relase is available. This may have newer features, but is not guaranteed to be stable.

The latest nightly build is available as an archive. To install the latest nightly build:

 1. Open [Client nightly builds](http://repository-zanata.forge.cloudbees.com/snapshot/org/zanata/zanata-cli/).
 1. Open the directory showing the highest version number.
 1. Download either of the distributable archives (ending with `-dist.zip` or `-dist.tar.gz`).
 1. Extract the contents of the archive to your location of choice.
 1. Create a symbolic link to the `zanata-cli` script in the bin directory of the extracted archive. e.g. from the archive directory, run `sudo ln -s bin/zanata-cli  /usr/local/bin/zanata-cli`

 1. (optional) you can also enable tab-autocomplete for the client if you use bash as your terminal shell. This can be done by copying or linking the `zanata-cli-completion` script from the bin directory to `/etc/bash_completion.d/`. e.g. `ln -s bin/zanata-cli-completion /etc/bash_completion.d/zanata-cli-completion`
