---
title: "Zanata Version 3.9.1 release announcement"
layout: post
categories:
- blog
tags:
- announcement
- release
- v3
author: Ding-Yi Chen
author_username: definite
---
zanata-server-3.9.3 is released and deploy to all our servers.

## Highlights

This release fixes the login problems for Fedora and Yahoo
authentication. As will as many UI changes and improvements to the web interface for web UI users, REST API users and system administrators.

### For Web UI End Users
* 0% matched translation will never bother you again in TM panel.
* The inactive timeout for login session is extended to 30 minutes.

### For Developers
* Review data and list of contributors for a project version are now available in REST API.
* Fix to upload translations on Wildfly 10.
* Docker support for developers to quickly build and run latest development.

### For System Admin
* Wildfly version should be updated to version 10.
* Migrate from Seam 2 to CDI.
* Display user email based on admin configuration.

## More About the Release

- [Release Note for 3.9.1](http://docs.zanata.org/en/latest/release-notes/#391)
- [Release Note for 3.9.0](http://docs.zanata.org/en/latest/release-notes/#390)
- [Download zanata-server-3.9.1](https://github.com/zanata/zanata-server/releases/tag/server-3.9.1)

