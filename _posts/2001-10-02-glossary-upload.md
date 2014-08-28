---
layout: help
title:  "Upload glossary"
categories:
- help
- glossary
---
### Prerequisite
See [glossary roles and permission]({{ site.url }}/help/glossary/glossary-roles-permission) for permission setup.

### Supported file format
#### PO
1. GNU Gettext-based PO file

#### CSV (comma-separated value), UTF-8 format
##### header row
1. locale columns: The locale header column must contain a valid locale code. At least one locale code is required for the glossary. First locale column will be used as source.
1. part-of-speech column (optional): The part-of-speech header column, when included, should contain only one value: pos.
1. description column (optional): The description header column, when included, should contain only one value: description.


##### data rows
1. terminology columns: Terminology in each row should correspond to the locale in the header. At least one term is required for a row to be valid.
1. part-of-speech column: The part-of-speech is an informational field that indicates the sense in which the terms in the row should be used. Sample parts-of-speech include adjective, adverb, noun, and verb.
1. description column: The description should provide any notes for the translator, including the meaning of the terms in the row.
<figure>
    <img alt="sample glossary csv file" src="{{ site.url }}/images/351-glossary-csv.png" />
    <figcaption>Valid glossary csv file</figcaption>
</figure>

### Upload via Web UI
1. Login into Zanata
1. Click `Glossary` menu.
1. Click on `More Actions` on top right corner of the table, follow by `Upload glossary` from the list.
<figure>
    <img alt="More action in glossary page" src="{{ site.url }}/images/351-glossary-upload.png" />
    <figcaption>More actions in glossary table</figcaption>
</figure>

1. A windows will popup, click on `choose file` to select your glossary file.
<figure>
 <img alt="Glossary upload windows" src="{{ site.url }}/images/351-glossary-upload-windows.png" />
</figure>

1. For PO file format, you will need to select **Source and Target languages** of the selected po file.
<figure>
 <img alt="Glossary upload windows, PO file" src="{{ site.url }}/images/351-glossary-upload-windows-po.png" />
</figure>

1. Click `Upload` button to start uploading selected glossary file.

### Upload via Zanata Maven client
The following instructions assume that you have installed and configured the Zanata Maven Plugin. Instructions for installation and configuration are available at [Installing the Maven Plugin]({{ site.url }}/help/maven-plugin/maven-plugin-install) and [Configuring the Maven Plugin]({{ site.url }}/help/maven-plugin/maven-plugin-config)

Command

```
mvn zanata:glossary-push -Dzanata.glossaryFile={filename} -Dzanata.sourceLang={source locale} -Dzanata.transLang={translation locale}
```
