---
layout: help
title:  "Delete Glossary"
categories:
- help
- glossary
---

Glossaries can be deleted by users with role *glossary-admin*. For more
information on roles, see [Glossary Roles and Permissions]({{ site.url }}/help/glossary/glossary-roles-permissions).

A glossary administrator can delete a glossary using the website or using the
command-line client. Deleting a glossary will remove all glossary entries for a
single language.


## Delete a glossary using the website

1. Log In to the Zanata website.
1. Click `Glossary` on the main menu.
1. Click on `Delete glossary` in the Glossary Options menu. To open the Glossary
Options menu, click the icon to the left of the glossary language you wish to
delete.

<figure>
    <img alt="Glossary options" src="{{ site.url }}/images/351-glossary-options.png" />
</figure>

1. Click `OK` to confirm deleting all glossary entries for the selected locale.


## Delete a glossary using the command-line client

You can use the command-line client to delete glossary entries for a single
locale, or to delete all glossary entries for all locales in a single operation.

The following instructions assume that you have installed and configured the
Zanata Maven Plugin. For instructions on installation of the plugin, see
[Installing the Maven Plugin]({{ site.url }}/help/maven-plugin/maven-plugin-install).
For instructions on configuration of the plugin, see
[Configuring the Maven Plugin]({{ site.url }}/help/maven-plugin/maven-plugin-config).


### Delete glossary entries by locale

To remove all glossary entries for a single locale, run the following command.
Substitute the locale of the glossary entries to delete in the place of
`{locale}`.

```
mvn zanata:glossary-delete -Dzanata.lang={locale}
```

### Delete all glossary entries in Zanata

To remove all glossary entries for all locales, run the following command.

```
mvn zanata:glossary-delete -Dzanata.allGlossary=true
```
