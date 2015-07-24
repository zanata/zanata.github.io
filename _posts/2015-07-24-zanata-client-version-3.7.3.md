---
title: "Zanata Client Version 3.7.3: Release Notes"
layout: post
categories:
- blog
tags:
- client
- announcement
- release
- v3
- v3.7
author: Ding-Yi Chen
author_username: definite
---

## What's New
<h5>Greatly decrease the download size</h5>
* [1124630](https://bugzilla.redhat.com/show_bug.cgi?id=1132271) - RFE: zanata-client should use jersey instead of resteasy

  This is achieved by using jersey instead of resteasy.


<h5>New way to install zanata-client</h5>
* [1229554](https://bugzilla.redhat.com/show_bug.cgi?id=1229554) - Package zanata-cli with 0install 
* dchen's [epel-zanata.repo](https://repos.fedorapeople.org/repos/dchen/zanata/epel-zanata.repo) for RHEL/CentOS 7 and 6


<h5>Able to specify minimum percentage required when pulled</h5>
* [1215274](https://bugzilla.redhat.com/show_bug.cgi?id=1215274) - Should be able to specify minimum percentage completion on pull
  Command looks like:

    zanata-cli pull --min-doc-percent $MIN_PERCENT 

<h4>Bugfixes</h4>
* [1222730](https://bugzilla.redhat.com/show_bug.cgi?id=1222730) - Java client missing useCache and purgeCache option
* [1241346](https://bugzilla.redhat.com/show_bug.cgi?id=1241346) - File mapping rule patter attribute is not recogized

