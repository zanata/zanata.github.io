---
layout: help
title:  "Copy Trans Explained"
categories:
- help
- reuse

copytrans: "Copy Trans"
---

{{page.copytrans}} works by trying to find a good match for every string in a document in every language.

For each string that does not yet have a translation in 'Translated' or 'Approved' state, {{page.copytrans}} will search for strings with exactly the same content that have a translation, checking every string in every project in Zanata that has a translation in 'Translated' or 'Approved' state. When a matching string is found, {{page.copytrans}} will check a set of conditions to decide what should be done with it. This is repeated for each language. You can modify what {{page.copytrans}} does with each condition using instructions in [Translation Reuse with Copy Trans]({{ site.url }}/help/reuse/copytrans-use).

*Note:* Only strings that have exactly the same source content are considered for {{page.copytrans}}. If you want to use strings that are not exactly the same, the Translation Memory Merge feature in the editor can be used.

If any 'Translated' or 'Approved' strings have the same source content and get past all the conditions, one of them will be used. If there is only one such string, it will be used. If there are multiple strings, the closest match is selected by:

 1. If there are any strings that pass all of the conditions without matching a `Don't Copy` or `Copy as Fuzzy` condition, the newest one will be used.
 1. Otherwise, if there are any strings that get to rule 5 without matching a `Don't Copy` rule, but match a `Copy as Fuzzy` rule, a 'Fuzzy' string will be used. If there is more than one such string, the strings that match earlier `Copy as Fuzzy` conditions take lower priority. The highest priority string is used, or if multiple strings share the highest priority, the newest of them will be used.
 1. If all strings match one or more `Don't Copy` rules, no translation will be copied for the text flow.

This process is repeated for each text flow in the uploaded document, or, if {{page.copytrans}} is run against a project-version, for each text flow in each document in the project-version.

*Note:* that if there is already a 'Fuzzy' translation for a text flow, it may be overwritten by a 'Translated' or 'Approved' translation. Because of this, copytrans is best used before translation and review work is initiated on a project, since overwriting half-finished translations and rejected strings could interfere with translator and reviewer workflows and cause confusion.
