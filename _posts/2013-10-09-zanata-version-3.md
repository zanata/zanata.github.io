---
title: "Zanata Version 3: Release Notes"
layout: post
categories:
- blog
tags:
- announcement
- release
- v3
---

Very soon, [translate.zanata.org](http://translate.zanata.org) will be upgraded to version 3. Zanata version 3 adds some major features and improvements over the currently deployed version 2.2.2.

Here is a preview of what is on the way in the new version:


### Updated Style

The most immediately noticeable improvement is the new visual style: we have changed our logo and colour scheme to improve readability of the site, and have started improvements to the layout to make Zanata easier to navigate.

Use the menu at the top right to get back to the user dashboard (see below), change your settings, or log out. The rest of the menus and screens should already be familiar.

![Dashboard link in user menu]({{ site.url }}/images/302-dashboard-menu.png)


### User Dashboard

Finding the content you care about is now much faster with the addition of the user dashboard. The dashboard shows your projects and shows your recent activity, so you can get straight back to anything you have been recently working on. For more, see [User Dashboard]({{ site.url }}/help/dashboard/user-dashboard).

![User Dashboard]({{ site.url }}/images/302-user-dashboard-full.png)


### Translation Review

For projects that need an extra level of checking, we have added a translation review workflow. Review can be turned on for a project, allowing reviewers (nominated by translation team coordinators) to mark translated strings as approved, or provide a message indicating what work is still required. See [Review Workflow]({{ site.url }}/help/review/review-workflow) for more information.

![New review buttons in the editor]({{ site.url }}/images/302-editor-approve-button.png)


### Translation Memory Import and Export

It is now possible to export the translation memory for a project or project-version. This will produce a file in TMX format. TMX generated in other systems can be imported to Zanata and will show translation memory matches in the editor. TMX import is currently restricted to administrators since it affects all users, so use the [Contact Admin](https://translate.zanata.org/zanata/help/contact) link in the 'Help' section 


### Other Changes

Version 3 comes with more changes the help to improve performance and stability, such as updating to a faster server platform. For more information, see the [Zanata Changelog](https://raw.github.com/zanata/zanata-server/master/CHANGELOG.md)
