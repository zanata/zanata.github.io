---
title: Features
layout: features
---
<div class="txt--hero l--push-bottom-1">
    <h1 class="txt--align-center gamma"><span class="heading--secondary">We have features…</span> for everyone</h1>
</div>

<hr>

<h2 class="txt--align-center alpha heading--secondary">For Translators</h2>

<div class="g l--push-top-2">
    <div class="g__item w--1-3">
        <img src="{{ site.url }}/images/features/focus-on-translation.png" alt="Screenshot">
    </div>
    <div class="g__item w--2-3">
        <h3 class="l--push-top-0">Focus on Translation</h3>
        <!--
         - plural support
         - dashboard (recent addition)
        -->
        <p>Zanata handles the overall workflow so that translators can be completely focused on translating, not on tools or formats:</p>
        <ul>
           <li>Zanata's Editor works on any computer with a web browser; no installation is needed.</li>
           <li>Translations can be written in Zanata without the need to work with version control systems, esoteric document formats or confusing email workflows.</li>
           <li>Zanata's User Dashboard provides a shortcut to jump straight to any current job.</li>
           <li>Plurals are handled natively in Zantat's Editor.</li>
        </ul>
    </div>
</div>

<div class="g--rev l--push-top-2">
    <div class="g__item w--1-3">
        <img src="{{ site.url }}/images/features/work-together.png" alt="Screenshot">
    </div>
    <div class="g__item w--2-3">
        <h3 class="l--push-top-0">Work Together</h3>
        <!--
          - concurrent editing of the same document, immediately shared
          - position indicators
          - conflict resolution
          - chatroom
        -->

        <p>Multiple translators can work on the same document using Zanata's Editor. Zanata's Editor provides a range of features to help translators work together effectively:</p>

        <ul>
            <li>Translations are visible to all translators as soon as they are saved.</li>
            <li>Markers indicate when a passage is being edited by other translators.</li>
            <li>A simple dialog prevents work being lost if a conflict occurs.</li>
            <li>Each language in the project has a chatroom for realtime communication.</li>
        </ul>
    </div>
</div>

<div class="g l--push-top-2">
    <div class="g__item w--1-3">
        <img src="{{ site.url }}/images/features/high-quality-suggestions.png" alt="Screenshot">
    </div>
    <div class="g__item w--2-3">
        <h3 class="l--push-top-0">High Quality Suggestions</h3>
        <!--
         - shared translation memory, updated in realtime
         - TM merge - re-use translations from similar documents
        -->
        <p>Translators can avoid writing the same translation twice by using Zanata's Translation Memory (TM). Zanata's TM is a powerful tool for translation reuse:</p>
        <ul>
           <li>The TM finds the best translation matches out of all the translations in the whole system.</li>
           <li>The TM is built into Zanata's Editor, allowing a streamlined workflow.</li>
           <li>The TM is updated in realtime to allow instant reuse.</li>
           <li>Each page of translations can be easily pre-filled with the best translation matches.</li>
        </ul>
    </div>
</div>

<div class="g--rev l--push-top-2">
    <div class="g__item w--1-3">
        <img src="{{ site.url }}/images/features/information-at-your-fingertips.png" alt="Information at Your Fingertips">
    </div>
    <div class="g__item w--2-3">
        <h3 class="l--push-top-0">Information at Your Fingertips</h3>
        <!--
         - syntax highlighting
         - live statistics
         - translation history
         - glossary
        -->

        <p>Zanata's Editor provides easy access to a range of useful information so that translators can work without disruptive context changes:</p>

        <ul>
            <li>Zanata shows live translation statistics and remaining work estimation for each document and the whole project, updated in realtime.</li>
            <li>Syntax highlighting is available to support technical translations.</li>
            <li>History for each translation can be accessed with a single click, to quickly see when it was changed and reviewed.</li>
            <li>A glossary is integrated into the editor for convenient look-up of terms.</li>
        </ul>
    </div>
</div>

<div class="g l--push-v-2">
    <div class="g__item w--1-3">
        <img src="{{ site.url }}/images/features/support-for-high-quality-translations.png" alt="Support for High Quality Translations">
    </div>
    <div class="g__item w--2-3">
        <h3 class="l--push-top-0">Support for High Quality Translations</h3>
        <!--
         - project-wide search & replace
         - review workflow
        -->
        <p>Zanata's Editor provides a set of features to support high translation quality:</p>
        <ul>
           <li>Validatiors run as translations are typed in the Editor, immediately reporting common mistakes and problematic items.</li>
           <li>The Editor's review workflow provides a way to ensure all translations meet the required standard.</li>
           <li>The Editor allows replacement of words through every document in a project, with full control, review and undo to avoid any unwanted changes; easily and confidently update terminology and fix mistakes.</li>
        </ul>
    </div>
</div>

<hr>

<h2 class="txt--align-center alpha heading--secondary">Writers and Developers</h2>

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
