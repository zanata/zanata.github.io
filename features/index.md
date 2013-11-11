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

Zanata handles the overall workflow so that translators can be completely focused on translating, not on tools or formats:-

 - Zanata's Editor works on any computer with a web browser; no installation is needed.
 - Translations can be written in Zanata without the need to work with version control systems, esoteric document formats or confusing email workflows.
 - Zanata's User Dashboard provides a shortcut to jump straight to any current job.
 - Plurals are handled natively in Zantat's Editor.


### Work Together
<!--
 - concurrent editing of the same document, immediately shared
    - position indicators
    - conflict resolution
    - chatroom
  -->

Multiple translators can work on the same document using Zanata's Editor. Zanata's Editor provides a range of features to help translators work together effectively:-

 - Translations are visible to all translators as soon as they are saved.
 - Markers indicate when a passage is being edited by other translators.
 - A simple dialog prevents work being lost if a conflict occurs.
 - Each language in the project has a chatroom for realtime communication.


### High Quality Suggestions
<!--
 - shared translation memory, updated in realtime
 - TM merge - re-use translations from similar documents
-->

Translators can avoid writing the same translation twice by using Zanata's Translation Memory (TM). Zanata's TM is a powerful tool for translation reuse:-

 - The TM finds the best translation matches out of all the translations in the whole system.
 - The TM is built into Zanata's Editor, allowing a streamlined workflow.
 - The TM is updated in realtime to allow instant reuse.
 - Each page of translations can be easily pre-filled with the best translation matches.


### Information at Your Fingertips
<!--
 - syntax highlighting
 - live statistics
 - translation history
 - glossary
-->

Zanata's Editor provides easy access to a range of useful information so that translators can work without disruptive context changes:-

 - Zanata shows live translation statistics and remaining work estimation for each document and the whole project, updated in realtime.
 - Syntax highlighting is available to support technical translations.
 - History for each translation can be accessed with a single click, to quickly see when it was changed and reviewed.
 - A glossary is integrated into the editor for convenient look-up of terms.



### Support for High Quality Translations
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