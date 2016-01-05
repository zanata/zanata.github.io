---
title: "Zanata Server Version 3.8.2: Release Notes"
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
not only see the actual terms, but also add the new terms straight on the web-UI.

<figure>
<img src="{{ site-url }}/images/posts/glossary-list.png" alt="Glossary list">
<figcaption>Glossary list in 3.8</figcaption>
</figure>



### Project Creation Permission
One of the popular requests was to grant the project creation only the certain sets of the users
to prevent spam projects.

Now admin can grant the trustworthy users with project creation right.
Note that existing users in our public servers will still have project creation permission
at the moment.

<figure>
<img src="{{ site-url }}/images/posts/project-creator.png" alt="Project creator permission">
<figcaption>Project creator permission in dialog Manage User</figcaption>
</figure>


### Search User in Main Search Bar
The main search bar seen on the top of the page can now be used to search users.

<figure>
<img src="{{ site-url }}/images/posts/search-user.png" alt="Search user">
<figcaption>Main search bar can search user </figcaption>
</figure>


## What is New
* [1213630](https://bugzilla.redhat.com/show_bug.cgi?id=1213630) - Webhook header needs to include cryptographic signature in header for identification
* [1214502](https://bugzilla.redhat.com/show_bug.cgi?id=1214502) - RFE: Grant project creation permission to certain sets of users
* [1224912](https://bugzilla.redhat.com/show_bug.cgi?id=1224912) - Filter "Last modified by translators other than &lt;user&gt;"
* [1233524](https://bugzilla.redhat.com/show_bug.cgi?id=1233524) - Update project search page to include user
* [ZNTA-108](https://zanata.atlassian.net/browse/ZNTA-108) - Improved glossary management: add, edit and delete individual glossary entries

## More About the Release
- [Release Note for 3.8.2](http://docs.zanata.org/en/latest/release-notes/#382)

- [Download zanata-server-3.8.2](https://github.com/zanata/zanata-server/releases/tag/server-3.8.2)

