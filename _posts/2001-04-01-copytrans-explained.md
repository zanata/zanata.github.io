---
layout: help
title:  "Copy Trans Explained"
categories:
- help
- reuse

copytrans: "Copy Trans"
---

{{page.copytrans}} works by trying to find a good match for every string in a document in every language.

For each string that does not yet have a translation in either a "Translated" or "Approved" state, {{page.copytrans}} searches for strings with exactly the same content that have a translation, and checks every string in every project in Zanata that has a translation in either a "Translated" or "Approved" state. When {{page.copytrans}} finds a matching string,  it checks a set of conditions to determine the next step. This is repeated for each language.

Use the instructions in [Translation Reuse with Copy Trans]({{ site.url }}/help/reuse/copytrans-use) to modify what {{page.copytrans}} does with each condition.

*Note:* {{page.copytrans}} only considers strings that have exactly the same source content. If you want to use strings that are not exactly the same, use the Translation Memory Merge feature in the editor.

If any "Translated" or "Approved" strings have the same source content and satisfy all the conditions, one of these strings will be used. If there is only one such string, it will be used. If there are multiple strings, the closest match is selected by:

 1. If any strings satisfy all conditions without matching a `Do not Copy` or `Copy as Fuzzy` condition, the latest translation is used.
 1. Otherwise, if any strings reach rule 5 without matching a `Do not Copy` rule, but match a `Copy as Fuzzy` rule, a "Fuzzy" string is used. If there is more than one such string, the strings that match later `Copy as Fuzzy` conditions take higher priority. The highest priority string is used, or if multiple strings share the highest priority, the string with the latest translation is used.
 1. If all strings match one or more `Do not Copy` rules, no translation is copied for the text flow.

This process is repeated for each text flow in the uploaded document, or, if {{page.copytrans}} is run against a project version, for each text flow in each document in the project version.

*Note:* If a "Fuzzy" translation already exists for a text flow, it may be overwritten by a "Translated" or "Approved" translation. Consequently, {{page.copytrans}} is best used before translation and review work is initiated on a project, because overwriting partly-completed translations and rejected strings could interfere with translator and reviewer work flows and cause confusion.
