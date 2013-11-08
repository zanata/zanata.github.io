---
title: Features
layout: page
---

## Translators


### Focus on Translation
<!--
 - plural support
 - dashboard (recent addition)
-->

Work with Zanata's rich editor from any browser. No need to install or update applications. No need to work with email or version control systems. No need to learn esoteric document formats. You can be completely focused on the translation, not the tools or formats.
User dashboard lets you quickly get back to translating your current projects.

Support for plurals natively in the editor.


### Work together with ease
<!--
 - concurrent editing of the same document, immediately shared
    - position indicators
    - conflict resolution
    - chatroom
  -->

Zanata's online editor allows multiple translators to work on the same document without stepping on each other's toes. Indicators show which passages are being edited by other translators, other people's translations are visible as soon as they are saved, conflicts are easily resolved, and a chatroom is provided for each language in the project for realtime collaboration.


*No installation needed, works in a web browser*



### High Quality Suggestions
<!--
 - shared translation memory, updated in realtime
 - TM merge - re-use translations from similar documents
-->

Zanata's editor has a built-in translation memory that finds the best translation matches out of all the translations in the whole system. The translation memory is updated in realtime, and each page of translations can be pre-populated with the best match. No need to write the same translation twice.


### Information at your fingertips
<!--
 - syntax highlighting
 - live statistics
 - translation history
 - glossary
-->

Zanata shows live translation statistics and remaining work estimation for each document and the whole project, updated in realtime. Syntax highlighting is available to support technical translations. Trace the history of each individual translation to see when they were changed and reviewed. Look up terms in the glossary, conveniently integrated into the editor.



### Support for High Quality translations
<!--
 - project-wide search & replace
 - review workflow
-->

Review tools to ensure all translations meet the required standard. Validatiors run in realtime, immediately reporting common mistakes and problematic items. Replace words through every document in a project to easily update terminology and fix mistakes. The process allows full control, review and undo to avoid any unwanted changes.


## Writers and Developers


### Automated Workflows

<!--
 - CLI client (fedora package, downloadable script)
 - Maven Plugin, supports multi-module projects
 - REST API for push, pull, stats
 - skynet integration
-->

Zanata's command-line client can be easily integrated into scripts and used in continuous integration. For Maven projects, Zanata provides a Maven Plugin that can support both simple and multi-module Maven projects. Zanata also has a REST API for scripting and integration with other tools.


### Translation Reuse
<!--
 - automatic reuse (copytrans), configurable
-->

Leverage the wealth of translations already on Zanata: Zanata can automatically copy matching translations from its translation memory to any text you upload, using your configured rules for match quality.


### Quality Control
<!--
 - enforced validations (TODO check that it is deployed before including in feature highlight)
 - translation reviews (optional)
 - TMX import/export (TODO put this in translator section as well)
 - Project Groups
 - Access control: Fedora projects limited to Fedora logins
-->

Ensure that translations can never break your build by enforcing relevant validations. Easily add a review phase to your project to ensure translations are to a high standard. Upload your existing translations and translation memory to Zanata to keep translations consistent. Use project groups to source translations form your trusted community.


### Major Formats Supported
<!--
 - supports Gettext(PO), Properties, XLIFF, LibreOffice (ODT, etc.), Mozilla DTD
 - publican/docbook workflow
 - smart merge of PO files after offline translation
 - preserves PO translation credits
 - ignore outdated translations in uploaded Properties files
-->

Zanata supports common translation formats for documentation and software. Supported formats include Gettext Portable Object (.po), Java Properties (.properties), XLIFF, Mozilla DTD, LibreOffice (.odt .fodt .odp .fodp .ods .fods .odg .fodg .odb .odf) and plain text (.txt). Zanata allows translation of .po files offline, perserving translator credits and using a smart merge algorithm for uploaded translations.

<!--
## General

 - Very large documents and projects supported (REST and editor)
 - Login systems supported:
    - username/password (native Zanata)
    - OpenID: Google, Yahoo, Fedora
    - Kerberos
    - nukes (jboss.org)

## This is not really a feature

 - built and supported by Red Hat engineers
    - resources to respond to new feature requests (this is probably misleading)
    - dedicated development team without the cost of commercial tools

-->