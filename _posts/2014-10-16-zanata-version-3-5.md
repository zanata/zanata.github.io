---
title: "Zanata Version 3.5: Release Notes"
layout: post
categories:
- blog
tags:
- announcement
- release
- v3
author: Luke Brooker
author_username: lukebrooker
---

<p class="txt--lead">We've received some great feedback in the previous release that has helped us create or improve this releases features. We hope you find them useful. As always, we'd love to hear how these features affect you and if there is anything we can do better.</p>

## What's New

- [Multiple Source Document Uploads](#multiple-source-document-uploads)
- [Guided Project Set-up for CLI Users](#guided-project-set-up-for-cli-users)
- [Redesigned Account Merge](#redesigned-account-merge)
- [Fork/Copy Previous Versions of a Project](#fork-copy-previous-versions-of-a-project)
- [Project/Version Page Enhancements](#project-version-page-enhancements)
- [Minor Enhancements](#minor-enhancements)
- [Infrastructure Change](#3-5-infrastructure-change)
- [Bug Fixes](#3-5-bug-fixes)


<h3 id="multiple-source-document-uploads">Multiple Source Document Uploads</h3>

You can now upload multiple source documents at once through the web interface.

<figure>
    <img src="{{ site-url }}/images/posts/mulltifile-upload-step-1.jpg" alt="Step 1">
    <figcaption>Click the “+”(Upload Document) button on the source document settings screen.</figcaption>
</figure>

<figure>
    <img src="{{ site-url }}/images/posts/mulltifile-upload-step-2.jpg" alt="Step 2">
    <figcaption>Either drag and drop or select multiple documents from your system documents picker.</figcaption>
</figure>

<figure>
    <img src="{{ site-url }}/images/posts/mulltifile-upload-step-3.jpg" alt="Step 3">
    <figcaption>Once you have added all the documents you need, select the “Upload Documents” button.</figcaption>
</figure>

<figure>
    <img src="{{ site-url }}/images/posts/mulltifile-upload-step-4.jpg" alt="Step 4">
    <figcaption>You will see the progress of your upload until completion.</figcaption>
</figure>

<figure>
    <img src="{{ site-url }}/images/posts/mulltifile-upload-step-5.jpg" alt="Step 5">
    <figcaption>Select “done” to close the modal and view your new document list.</figcaption>
</figure>

#### Related

- [1066694](https://bugzilla.redhat.com/show_bug.cgi?id=1066694) - As a project maintainer I would like to upload multiple source files simultaneously

<h3 id="guided-project-set-up-for-cli-users">Guided Project Set-up for CLI Users</h3>

Command line user can now setup their projects from the CLI quickly with a new command, `zanata-cli init`. Check out the guide on [initialising a project]({{ site-url }}/help/cli/cli-init/) and start saving time on the command line.

#### Related

- [1110627](https://bugzilla.redhat.com/show_bug.cgi?id=1110627) - As a command line user I would like to be guided in setting up a project

<h3 id="redesigned-account-merge">Redesigned Account Merge</h3>

If you've ever had problems with multiple accounts you may have lost track of (this can happen if an extra open id account is not attached properly to your primary account), it should now be easier to merge your accounts.

<figure>
    <img src="{{ site-url }}/images/posts/merge-acounts-step-1.jpg" alt="Step 1">
    <figcaption>Select “Merge accounts” at the bottom of your account settings page.</figcaption>
</figure>

<figure>
    <img src="{{ site-url }}/images/posts/merge-acounts-step-2.jpg" alt="Step 2">
    <figcaption>Choose the open id account you would like to merge into you current (logged into) account.</figcaption>
</figure>

<figure>
    <img src="{{ site-url }}/images/posts/merge-acounts-step-3.jpg" alt="Step 3">
    <figcaption>Confirm the account details.</figcaption>
</figure>

<figure>
    <img src="{{ site-url }}/images/posts/merge-acounts-step-4.jpg" alt="Step 4">
    <figcaption>Your account will be connected to your logged in account.</figcaption>
</figure>

#### Related

- [1110048](https://bugzilla.redhat.com/show_bug.cgi?id=1110048) - Redesign account merge page

<h3 id="fork-copy-previous-versions-of-a-project">Fork/Copy Previous Versions of a Project</h3>

When you create a new version, you can now base it on a previous version.

<figure>
    <img src="{{ site-url }}/images/posts/copy-version-step-1.jpg" alt="Step 1">
    <figcaption>On your projects page, select the “…”(More) dropdown and then select “New Version”.</figcaption>
</figure>

<figure>
    <img src="{{ site-url }}/images/posts/copy-version-step-2.jpg" alt="Step 2">
    <figcaption>Choose “Copy from previous version”(selected by default) then from the list choose the version you would like to copy(latest selected by default). Now select “Create Version” and the version copy will begin.</figcaption>
</figure>

#### Related

- [1104015](https://bugzilla.redhat.com/show_bug.cgi?id=1104015) - Fork/copy from previous version with source and translation.

<h3 id="project-version-page-enhancements">Project/Version Page Enhancements</h3>

#### More Sorting Options for Document Lists

In the previous release we held back some sorting options to fix a performance problem. The problem is now fixed and we have added the extra options back.

#### More Items for Language and Document List Page

For the same performance problems we had limited the amount of documents/languages listed per page. This has now been bumped up to 100 per page.

#### Related

- [1110959](https://bugzilla.redhat.com/show_bug.cgi?id=1110959) - Add in more sorting options in version page

<h3 id="minor-enhancements">Minor Enhancements</h3>

#### Editor Design Update

Some small tweaks have been made to the current editor to bring in some concepts coming in an major editor redesign.

#### Glossary Design Update

The glossary page brings has been updated to be closer to the latest Zanata design.

#### Other Features

- Subtitle Format (.srt) is now supported
- JBoss SSO Login has been improved

#### Related

- [1131300](https://bugzilla.redhat.com/show_bug.cgi?id=1131300) - Update on editor UI
- [1122363](https://bugzilla.redhat.com/show_bug.cgi?id=1122363) - Update glossary page view
- [1062835](https://bugzilla.redhat.com/show_bug.cgi?id=1062835) - SubRip Text (.srt) subtitle format support
- [1110175](https://bugzilla.redhat.com/show_bug.cgi?id=1110175) - Add a JBoss SSO Login module

<h3 id="3-5-infrastructure-change">Infrastructure change</h3>

- Now requires (i.e. is tested on) OpenJDK 7

<h3 id="3-5-bug-fixes">Bug fixes</h3>

* [971652](https://bugzilla.redhat.com/show_bug.cgi?id=971652) - \[Document List\] Clicking column header "Complete" mistakenly sort by other column you sort
* [1060629](https://bugzilla.redhat.com/show_bug.cgi?id=1060629) - Manage Languages breadcrumb takes user to the wrong page
* [1094094](https://bugzilla.redhat.com/show_bug.cgi?id=1094094) - Copy Translations does not update the shown stats, if the language list is already loaded
* [1097470](https://bugzilla.redhat.com/show_bug.cgi?id=1097470) - When adding/removing maintainers in group, maintainer list doesn't update
* [1098394](https://bugzilla.redhat.com/show_bug.cgi?id=1098394) - No url validation on project homepage field
* [1098404](https://bugzilla.redhat.com/show_bug.cgi?id=1098404) - Project search resizes in the middle of clicking a result, preventing the click
* [1098407](https://bugzilla.redhat.com/show_bug.cgi?id=1098407) - Copy Translations box does not close if process halted via Process Manager
* [1099278](https://bugzilla.redhat.com/show_bug.cgi?id=1099278) - Changing email address produces invalid email
* [1099736](https://bugzilla.redhat.com/show_bug.cgi?id=1099736) - Increase cache retention for statistics
* [1102455](https://bugzilla.redhat.com/show_bug.cgi?id=1102455) - \[Search Field\] Failed to search the project by whole project name that contains spaces ' ' and hyphen '-'
* [1097552](https://bugzilla.redhat.com/show_bug.cgi?id=1097552) - Obsolete groups sometimes not visible to maintainer
* [1102488](https://bugzilla.redhat.com/show_bug.cgi?id=1102488) - \[zanata:stat\] Failed to return proper error message when getting stat for non-exists projects and versions
* [1101803](https://bugzilla.redhat.com/show_bug.cgi?id=1101803) - TMX clear function doesn't work from UI
* [1103547](https://bugzilla.redhat.com/show_bug.cgi?id=1103547) - Empty document statistic should show "No content" in version tabs
* [978618](https://bugzilla.redhat.com/show_bug.cgi?id=978618) - Accidental broken feature - admin can change usernames
* [1067288](https://bugzilla.redhat.com/show_bug.cgi?id=1067288) - Reduce size of zanata.war; exclude unused dependencies
* [1110599](https://bugzilla.redhat.com/show_bug.cgi?id=1110599) - Remove unused page in Zanata
* [1103940](https://bugzilla.redhat.com/show_bug.cgi?id=1103940) - Remove info level notification popup from the editor
* [1011310](https://bugzilla.redhat.com/show_bug.cgi?id=1011310) - Unhandled exception: Mail service is down
* [995904](https://bugzilla.redhat.com/show_bug.cgi?id=995904) - Unnecessary ellipsis on short TM source name in editor
* [994293](https://bugzilla.redhat.com/show_bug.cgi?id=994293) - Cancelling an upload causes a database lock exception
* [973509](https://bugzilla.redhat.com/show_bug.cgi?id=973509) - User not aware they can use other characters in Group ID
* [1112041](https://bugzilla.redhat.com/show_bug.cgi?id=1112041) - Upload feature should handle files that are deleted before the process begins nicely
* [993445](https://bugzilla.redhat.com/show_bug.cgi?id=993445) - User can successfully upload a txt file that doesn't exist
* [1130797](https://bugzilla.redhat.com/show_bug.cgi?id=1130797) - Cache document statistic and overflow to disk
* [1128954](https://bugzilla.redhat.com/show_bug.cgi?id=1128954) - Convoluted way of opening docs from groups
* [1120034](https://bugzilla.redhat.com/show_bug.cgi?id=1120034) - Pushing translations is too slow
