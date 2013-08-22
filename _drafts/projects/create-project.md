---
layout: post
title:  "Project Creation"
categories:
- help

---

Anyone with an account can create a project in Zanata. The first step is to create a project:

 1. **Create a project.**
 1. Create a version under the project (see [Version Creation][]).
 1. Add documents to the version.
   - Using the website
   - Using the command-line client

# Creation through the UI:

 - sign in as any user
 - go to "Create a New Project" page by:
   - (on dashboard) click `create your own` at the bottom of the project list
   - (on Projects page) click `Create project`
 - enter id that will show in the project url
 - enter name that will be displayed in project list etc.
 - maybe enter description
 - `Project Type` is important to select, so that config files will have all required information and all downloads are available.
   - link to wiki page for `Project Types`
 - view source files: if the project source files are available for viewing on the Internet, put a URL here that translators can use to see the original files (this can sometimes be useful for clarifying translations?)
   - e.g. Zanata's source files can be viewed at `some git url` so that is what we enter here for `zanata-server`
 - source download/checkout is for use by tools to fetch the source files.
   - e.g. Zanata's source can be fetched using the `git` tool by running `git clone blablabla` so for zanata-server we enter `blablabla`
 - Homepage Content is optional. If included, it is shown at the top of the page in Zanata for the project.
 - Status should usually be `ACTIVE`, but you may want to temporarily set to `READONLY` later if translation for the project is finalized.
 - Custom locales: server default will be used if these are not specified.
 - Restrict roles: I think this is for roles that represent membership of a group such as Fedora, otherwise probably don't use it. (BUG: it is not clear whether checking a box prevents or allows access. Logic implies restrict, but wording could also be interpreted as selecting the roles that have access). Does checking/unchecking admin actually prevent admin access to the project? It had better not. Seems like excessive overloading of roles here.
 - Custom validations: not enforced at this stage but should help translators to avoid breaking your build/layout. Recommended settings for:
   - all: leading/trailing newline, tab characters
   - gettext & podir: printf variables, positional printf
   - podir: HTML/XML tags
   - java properties: java variables
   - libreoffice documents: HTML/XML tags

(NOTE: we really should pre-select some validations based on the project type, possibly in response to clicking a `recommended settings` button)

 - click `save` to create the project (fix any validation errors that are shown).


# Creation from command line

Projects can also be created using the command-line client. Some of the options (which?) are not available through command line.