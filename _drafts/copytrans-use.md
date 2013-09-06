---
layout: help
title:  "Translation Reuse with Copy Trans"
categories:
- help
- reuse

copytrans: "Copy Trans"
---

{{page.copytrans}} is a service that finds valid translations for documents by finding matching strings in other documents that are already translated.

{{page.copytrans}} can save a lot of translation effort when adding a new version of a project that has been translated in Zanata. Since many of the strings will usually be the same between versions version, many translations can be safely copied from the previous version.

{{page.copytrans}} will usually run automatically when a document is uploaded from the cli-client. When this happens the {{page.copytrans}} Options for the project are used. {{page.copytrans}} can also be run manually against a project-version.


Before setting {{page.copytrans}} Options, it is useful to have an understanding of the {{page.copytrans}} process. For a detailed explanation, see [Copy Trans Explained]({{ site.url }}/help/reuse/copytrans-explained).


## {{page.copytrans}} Options


To see {{page.copytrans}} Options for a project, navigate to the project page and click `Copy Trans Options`.

![Copy Trans Options button on Project page]({{ site.url }}/images/302-project-copy-trans-options.png)

The conditions to check on each potentially matching string are shown on the left. Actions to take can be selected to the right of each condition.

![Example of Copy Trans Options]({{ site.url }}/images/302-copytrans-options-newversion.png)

 - If a string matches any `Don't Copy` condition, it is not a valid match and will not be used.
 - If a string does not match any `Don't Copy` conditions, but matches one or more `Copy as Fuzzy` conditions, it may be reused but will have 'Fuzzy' state. Strings matching a `Copy as Fuzzy` condition will still be checked against all the remaining conditions.
 - The `Next Condition` option just turns off the condition, so it makes no difference whether a string matches the condition.


### {{page.copytrans}} Options Examples

#### Permissive Options

If `Next Condition` is selected for all conditions, only the required "On content mismatch" rule will be checked, so if a string has matching content it will bypass all the other conditions and be reused in 'Translated' state (or 'Approved' if your project requires review and the translation being copied is already in 'Approved' state). When there are multiple matches, the newest one will be used.

![Permissive Copy Trans Options]({{ site.url }}/images/302-copytrans-options-permissive.png)

#### Strict Options

If `Don't Copy` is selected for all conditions, a string must have matching content, have matching id, be from the same project and be from a document with the same and path, otherwise it will not be reused. If it is reused it will be in 'Translated' state. OR APPROVED

![Strict Copy Trans Options]({{ site.url }}/images/302-copytrans-options-strict.png)

#### Options for a New Version

For this example, consider that you have a new version of your project that has just been put in Zanata. The previous version is completely translated so you want to reuse the translations, but the new version uses a different directory structure so the document paths have all changed. The id for most strings is the same, but some strings have been added. To make sure it uses strings from the other version in your project only, set "On Project mismatch" to `Don't Copy`; To make sure the changed document paths don't matter, set "On Document Id mismatch" to `Next Condition`. Finally, since most string ids have not been changed, "On Context mismatch" is set to `Copy as Fuzzy`.

![Possible Copy Trans Options for a New Version]({{ site.url }}/images/302-copytrans-options-newversion.png)


## Running {{page.copytrans}}

{{page.copytrans}} can be run manually against a project-version.

On the project-version page, click `Copy Translations` to see and adjust the project {{page.copytrans}} options and a button to run {{page.copytrans}} against the version.

![Copy Translations button on version page]({{ site.url }}/images/302-version-copy-translations.png)

{{page.copytrans}} can take a long time to run, so a progress bar is shown on the version page while it is running.
