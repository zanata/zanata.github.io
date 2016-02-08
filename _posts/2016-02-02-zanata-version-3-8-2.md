---
title: "Zanata Version 3.8.2: Release Notes"
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

## Highlights

### Glossary: New Look and On-Line Editing

With this major glossary interface update, users with glossarist permission
can not only see the each term, but also edit them online.

<figure>
<img src="{{ site-url }}/images/posts/glossary-list.png" alt="Glossary list">
<figcaption>Glossary list in 3.8</figcaption>
</figure>

### Project Creation Permission

A popular request, was to grant project creation permissions to a specific set of users. This allows Zanata admins more control over the projects that can be created on their instance.

This has to be enabled by admins and will not affect any of the Zanata teams currently maintained instances.

<figure>
<img src="{{ site-url }}/images/posts/project-creator.png" alt="Project creator permission">
<figcaption>Project creator permission in dialog Manage User</figcaption>
</figure>

### Project Team Management

Project maintainers can now manage their own team of translators.

If you have your own trusted translators or reviewers, they no longer need to join a global language team.
Go to the **People** tab in project view, click **Add Someone**. On top of maintainers, you can now add translators, reviewers or translation maintainers (who can also add translator and reviewers).

<figure>
<img src="{{ site-url }}/images/posts/project-team-management.png" alt="Project team management">
<figcaption>Project team management</figcaption>
</figure>

### Search User in Main Search Bar

The main search bar seen on the top of the page can now be used to search users.

When you find the user you are looking for , you will be able to see a few more details and their recent translation/revieer contributions.

<figure>
<img src="{{ site-url }}/images/posts/search-user.png" alt="Search user">
<figcaption>Main search bar can search user </figcaption>
</figure>

## More Feature Details

* [1213630](https://bugzilla.redhat.com/show_bug.cgi?id=1213630) - Webhook header needs to include cryptographic signature in header for identification
* [1214502](https://bugzilla.redhat.com/show_bug.cgi?id=1214502) - RFE: Grant project creation permission to certain sets of users
* [1224912](https://bugzilla.redhat.com/show_bug.cgi?id=1224912) - Filter "Last modified by translators other than &lt;user&gt;"
* [1233524](https://bugzilla.redhat.com/show_bug.cgi?id=1233524) - Update project search page to include user
* [ZNTA-108](https://zanata.atlassian.net/browse/ZNTA-108) - Improved glossary management: add, edit and delete individual glossary entries

## More About the Release

- [Release Note for 3.8.2](http://docs.zanata.org/en/latest/release-notes/#382)
- [Download zanata-server-3.8.2](https://github.com/zanata/zanata-server/releases/tag/server-3.8.2)

