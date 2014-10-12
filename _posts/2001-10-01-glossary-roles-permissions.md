---
layout: help
title:  "Glossary Roles and Permissions"
categories:
- help
- glossary
---


There are 2 roles that can manage glossaries in Zanata,  **glossarist** and
**glossary-admin**. To request either of these roles, users should contact a
Zanata administrator. Administrators can be contacted using the `Contact Admin`
button in the `Help` section.


The following table shows which permissions are available to each role.

<table>
  <thead>
    <tr>
      <td>Role</td>
      <td><a href="{{ site.url }}/help/glossary/glossary-upload">Upload glossary</a></td>
      <td><a href="{{ site.url }}/help/glossary/glossary-edit">Edit glossary</a></td>
      <td><a href="{{ site.url }}/help/glossary/glossary-delete">Delete glossary</a></td>
    </tr>
  </thead>
  <tr>
    <td>glossarist</td>
    <td class='txt--align-center'><i class='i i--checkmark'/></td>
    <td class='txt--align-center'><i class='i i--checkmark'/></td>
    <td class='txt--align-center'><i class='i i--cancel txt--danger'/></td>
  </tr>
  <tr>
    <td>glossary-admin</td>
    <td class='txt--align-center'><i class='i i--checkmark'/></td>
    <td class='txt--align-center'><i class='i i--checkmark'/></td>
    <td class='txt--align-center'><i class='i i--checkmark'/></td>
  </tr>
</table>


<p class='message--warning'>
  The terms for a glossary are available to all projects within Zanata. Users
  should understand that glossary upload, edit and delete can affect all users
  and perform such actions responsibly.
</p>
