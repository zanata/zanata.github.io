---
layout: help
title:  Translating
categories:
- help
- translation
---

These instructions are for using the translation editor. Instructions for opening the translation editor can be found at [Preparing for Translation]({{ site.url }}/help/translation/preparing-for-translation).


## The Basics

The core part of the editor is the table of source strings and translations in the center. Other features are displayed around the editor table: at the top is search and filtering, on the right are alerts, chat and options (including validation options), and at the bottom are translation memory and glossary.

The basic workflow is to enter a translation in a translation text box, save the translation, then move to the next row and repeat until the document is translated.


## Source Strings

Source strings show the original text for which a translation is needed. The text itself is displayed within a text box, and cannot be changed. In addition to the source text, some other useful information is shown.

Line numbers are shown to the left of the source and translation text boxes. Long lines will be displayed over several lines in the text box, but will only have a single line number.

Whitespace characters are shown in source and translation text to allow accurate translation. Spaces are displayed with a faint grey underline, newlines are shown with a faint grey pilcrow character (¶) and tabs are shown with a faint grey right-arrow-to-bar character (⇥).

The string number within the document is shown below the source string for the currently selected line, along with the source comment if one exists. Clicking the string number causes some extra information about the string to be displayed.

To the left of the string number is a bookmark icon. Clicking the bookmark icon updates the URL so that you can create a link directly to the string.


## Translation Text Boxes

To the right of each source string is a text box showing the current translation (if one exists). To enter a translation, click this text box and start typing. You can also copy the source text to the text box as a starting point by clicking the 'Copy Source' arrow between the source and translation text boxes.

As you type, validations will run on the text you have entered. If any validations fail, warnings will be displayed below the text box. Warnings are cleared when the text no longer fails the validation.

When you have entered an accurate translation, you can save the translation using the "Save as Translated" icon to the right of the text box, or by pressing Ctrl+Enter. If you are not satisfied with a translation you have entered, you can save it in draft form using the "Save as Fuzzy" flag icon or clear it by pressing the cancel icon.

If another translator is editing the same translation, their name is shown in the top right of the translation text box. If the other user saves their translation while you are entering a translation, you will be shown a dialog with their translation and your unsaved translation. To keep their translation and discard your version, just close the dialog. To keep editing your translation, click `Copy to Editor` and continue working. It is advised not to edit a translation at the same time as another translator in order to avoid such conflicts and duplicated effort.







 - editor layout
  * source strings
  * translation text boxes
  * main buttons
  * indicators for other translators
  - filter checkboxes
  - alerts/settings/validation/chat
  - stats
  - search/doclist
  - key shortcuts
  - translation memory
  - glossary
  - bookmark links
  - comments and other info
