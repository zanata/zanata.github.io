---
layout: help
title:  "Supported Glossary File Formats"
categories:
- help
- glossary
---


Zanata supports glossary files in both PO and CSV formats.

## PO

A valid GNU Gettext-based PO file.


## CSV

Comma-separated value (CSV) files must use UTF-8 encoding, and must be formatted
with a valid header row and valid data rows. Most spreadsheet programs can save
in CSV format.


### Header Row

The first row of a CSV glossary file is the header row. The header row must have
the source locale code, then any number of other locale codes, then may have one
or two detail headers. Detail headers, when present, can appear in any order, but must
all appear after the locale headers.

Detail headers are "pos" for part-of-speech, and "description" for additional
descriptive detail about a term.

Here is an example header row:

```
en-US,es,ja,pt-BR,pos,description
```

This header row has:

1. The source locale, "en-US". Any valid locale can be used as the source locale.
1. Locale headers for 3 languages: Spanish (es), Japanese (ja) and Brazilian
   Portuguese (pt-BR). As with the source locale, these must be valid locale
   codes. There must be at least one locale header.
1. A part-of-speech header, "pos". This column is optional.
1. A description header. This column is optional.



### Data Rows

The values in each data row must correspond to the headers in the header row.

Here is an example of a valid header row and 2 valid data rows in a spreadsheet
program.

<figure>
    <img alt="sample glossary csv file" src="{{ site.url }}/images/351-glossary-csv.png" />
    <figcaption>Valid glossary csv file</figcaption>
</figure>

The row labeled "1" is the header row, and the rows labeled "2" and "3" are the
data rows.

1. terminology columns: Terminology in each row should correspond to the locale in the header. At least one term is required for a row to be valid.
1. part-of-speech column: The part-of-speech is an informational field that indicates the sense in which the terms in the row should be used. Sample parts-of-speech include adjective, adverb, noun, and verb.
1. description column: The description should provide any notes for the translator, including the meaning of the terms in the row.

