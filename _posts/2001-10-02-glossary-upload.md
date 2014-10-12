---
layout: help
title:  "Upload Glossary"
categories:
- help
- glossary
---


Glossaries can be uploaded by users with roles *glossarist* or *glossary-admin*.
For more information on these roles, see [Glossary Roles and Permissions]({{ site.url }}/help/glossary/glossary-roles-permissions).

The formats and structure for glossary files that may be uploaded are described
in [Supported Glossary File Formats]({{ site.url }}/help/glossary/glossary-formats).


## Upload via Web UI

1. Login to Zanata.
1. Click `Glossary` in the main menu.
1. Click on `More Actions` on top right corner of the "Glossary entries" table.

<figure>
    <img alt="More action in glossary page" src="{{ site.url }}/images/351-glossary-upload.png" />
    <figcaption>More actions in glossary table</figcaption>
</figure>

1. Click `Upload glossary` to open the upload dialog.
1. In the upload dialog, click `Choose File` and select the glossary file you
wish to upload.

<figure>
 <img alt="Glossary upload window" src="{{ site.url }}/images/351-glossary-upload-windows.png" />
</figure>

1. When a file has been selected, additional options are added to the dialog
depending on the glossary file type. For PO file format, you will need to select **Source and Target languages** of the selected po file. For CSV file format you may need to
change the value for "Comment column names" if the default names do not match
the column headings in your glossary file.

<figure>
 <img alt="Glossary upload window, PO file" src="{{ site.url }}/images/351-glossary-upload-windows-po.png" />
</figure>

1. Click `Upload` to start uploading selected glossary file.


## Upload via Zanata Maven client

The following instructions assume that you have installed and configured the
Zanata Maven Plugin. Instructions for installation and configuration are
available at [Installing the Maven Plugin]({{ site.url }}/help/maven-plugin/maven-plugin-install)
and [Configuring the Maven Plugin]({{ site.url }}/help/maven-plugin/maven-plugin-config)

To upload a glossary, run the following command, substituting the name of the
file in the place of `{filename}`, the source locale code in the place of
`{source locale}`, and the translation locale code in the place of
`{translation locale}`.

```
mvn zanata:glossary-push -Dzanata.glossaryFile={filename} \
    -Dzanata.sourceLang={source locale} -Dzanata.transLang={translation locale}
```
