---
title:  "Translation Reuse with Copy Trans"
last-updated: 2014-10-30
redirect_from: "/help/reuse/copytrans-explained/"

copytrans: "Copy Trans"
---

{{page.copytrans}} is a service that finds valid translations for documents by finding matching strings in other documents that are already translated.

{{page.copytrans}} can save a lot of translation effort when adding a new version of a project that has been translated in Zanata. Because many of the strings will usually be the same between versions, many translations can be safely copied from the previous version.

{{page.copytrans}} usually runs automatically when a document is uploaded using the cli-client. The {{page.copytrans}} Options for the project are used in this case. You can also run {{page.copytrans}} manually against a project version.


Before setting {{page.copytrans}} Options, it is useful to have an understanding of the {{page.copytrans}} process. For a detailed explanation, see [Copy Trans Explained]({{ site.url }}/help/reuse/copytrans-explained).


## {{page.copytrans}} Options


To see the {{page.copytrans}} Options for a project, navigate to the project page and click `Copy Trans Options`.

![Copy Trans Options button on Project page]({{ site.url }}/images/302-project-copy-trans-options.png)

The *Condition* column lists the conditions to check on each potentially matching string.  The *Action* column lists the options available whenever a condition is met.

![Example of Copy Trans Options]({{ site.url }}/images/302-copytrans-options-newversion.png)

 - If a string matches any `Do not Copy` conditions, it is not a valid match and is not used.
 - If a string does not match any `Do not Copy` conditions, but matches one or more `Copy as Fuzzy` conditions, it may be reused but will have a state of "Fuzzy". Strings matching a `Copy as Fuzzy` condition are still checked against all remaining conditions.
 - The `Next Condition` option disables the condition, consequently it makes no difference whether a string matches the condition or not.


### Examples of {{page.copytrans}} Options

#### Permissive Options

If `Next Condition` is selected for all conditions, only the required "On content mismatch" rule is checked. This means that if a string has matching content it bypasses all other conditions and is reused in a "Translated" state (or "Approved" if your project requires review and the translation being copied is already in "Approved" state). When there are multiple matches, the latest translation is used.

![Permissive Copy Trans Options]({{ site.url }}/images/302-copytrans-options-permissive.png)

#### Strict Options

If `Do not Copy` is selected for all conditions, a string must have matching content, a matching ID, be from the same project, and be from a document with the same name and path, otherwise it will not be reused. If all of the conditions are passed, the content is reused in a "Translated" state (or "Approved" if your project requires review and the translation being copied is already in "Approved" state).

![Strict Copy Trans Options]({{ site.url }}/images/302-copytrans-options-strict.png)

#### Options for a New Version

For this example, consider that you have a new version of your project in Zanata. The previous version is completely translated and you want to reuse the translations, but the new version uses a different directory structure. This means that the document paths have all changed. The ID for most strings is the same, but some new strings have been added. You should set up the options as follows:

1. To ensure that {{page.copytrans}} uses strings from the other version in your project only, set "On Project mismatch" to `Do not Copy`.
1. To ensure that the changed document paths do not affect the reuse process, set "On Document ID mismatch" to `Next Condition`.
1. Because most string IDs have not changed, set "On Context mismatch" to `Copy as Fuzzy`.

![Possible Copy Trans Options for a New Version]({{ site.url }}/images/302-copytrans-options-newversion.png)


## Running {{page.copytrans}}

You can run {{page.copytrans}} manually against a project version.

1. On the project version page, click `Copy Translations` in the `Actions` menu to open the `Copy Translations` page.
1. Select the appropriate action for each condition, and then click `Start`.

![Copy Translations button on version page]({{ site.url }}/images/302-version-copy-translations.png)

A progress bar on the version page displays the progress of the operation. Depending on the size of the project and the number of available translations, this process can take some time to complete.
