---
title: "Fedora Zanata Migration Survey Results"
layout: post
permalink: /blog/fedora-zanata-survey-results
categories:
- blog
tags:
- fedora
author: Luke Brooker
author_username: lukebrooker
---

*From October 7th to October 28th 2015 we put out [a survey](https://zanata.typeform.com/to/SAZvRP) to the Fedora community and received over 40 responses.*

First, we'd like to say thank you to everyone who took the time to complete the survey. We have lots of great feedback to help us understand the needs of the Fedora l10n community and improve Zanata to meet these needs.

In this post I’ll cover some overall statistics around the multiple choice questions and then summarise some of the more specific feedback and how it affects Zanata.

## The migration from Transifex to Zanata

Mailing lists were by far (61%) the most common place you heard about the Migration to Zanata, with the Magazine (15%) and Wiki (10%) coming distant runners-up. It seems like the mailing lists remain the best place to get news out to the l10n team.

93% of you thought the migration to Zanata went either very well (29%), well (17%), or  OK (46%). There is still room to improve here and I'll cover some specific feedback later. 91% were either very happy, happy or neutral with responses to your queries and doubts. To the 4 of you that were not satisfied, we'd love to hear from you about what went wrong, if we haven't already.

Some more specific feedback we received about the Migration was:

- Some would have liked a copy of the Transifex history for reference
- Some projects were not moved to Zanata. I'm not sure of the reason for this.
- More updates on the status of each project’s move to Zanata and when it was ready for translation

The Zanata team has taken this feedback on board and will use it to improve communications about the maintenance and operations of the Zanata instance.

## Using Zanata

We are happy to hear that over 50% of you have used Zanata more than 10 times (56%). And others are not too far behind. The majority (86%) of your experiences with Zanata have been either positive or OK. With 6 of you having negative experiences. This is still something we would love to improve, and we are grateful to have received lots of specific feedback to help us do just that.

## Improving Zanata

We've sorted the feedback to give us some clarity about where we need to focus. I'll start with the most common feedback we received.

### Language Teams / Project Management

By far the most common feedback we received was related to **better language team/project management features**. In this category we included:

- Team Activity
- Team Statistics
- Project Status
- Language-specific project list

These features are one of the major aspects of Zanata that we want to improve and it is great to have the Fedora community confirm their importance.

Team activity feedback is mainly related to being able to see what other members of your language team are working on, and helping each of you decide where your effort is best applied.

Statistics should allow users to see who is contributing to the team and in what capacity. There should be more statistics available for projects, teams and groups.

Project status features could relate to a specific "project" in Zanata or potentially groups. These would include things like minimum translation acceptance percentage & project/team/group milestones.

Language-specific project list was requested a lot, and at least easily seeing your own language without having to select it each time. We can achieve part of this with groups, but it is still less than ideal and still requires you to find your language. We are exploring some solutions for this problem, and will reach out when we have some concrete proposals.

You can view some [language team/project management related issues on our JIRA](https://zanata.atlassian.net/browse/ZNTA-318?jql=labels%20%3D%20languageteams). We'll add to this list over time. To join the planning process you can vote up issues, add comments, or if your concern or idea is not shown, add your own issue.

### Editor Improvements

- Variable handling
- Translation comments
- Search improvements
- Display options

We are constantly working to improve the editor, and have dozens of planned improvements to make. This feedback gives us a better idea of what to work on first.

You can view [editor related issues on our JIRA](https://zanata.atlassian.net/browse/ZNTA-739?jql=project%20%3D%20ZNTA%20AND%20component%20%3D%20Editor).

### Translation Memory

- Improved search results
- Customisation

Translation memory was noted as the most critical feature needed. Translation memory is something we still have a focus on and we hope to improve it in some upcoming releases. You can keep track of any [translation memory related issues on our JIRA](https://zanata.atlassian.net/browse/ZNTA-57?jql=project%20%3D%20ZNTA%20AND%20text%20~%20%22%5C%22TM%5C%22%22).

### Notifications

Something that we have been planning and discussing for a while is how best to implement notifications. We've known they are needed and hopefully the extra feedback we've received here will give us the push to start working on them.

### Getting started

To get started as a translator in the Fedora Zanata, we know there are quite a few steps involved. This is made longer again if you don't already have a Fedora account. We have a change in the next version of Zanata that will make joining a language team easier for both translators and team co-ordinators.

In the future, we may also look into simplifying account activations as well. Other than this, a lot of what is involved may come down to how the Fedora community runs. This is something we can work on as a community to improve.

### Fast, Reliable Servers

The problems that were identified are login failures, short authentication expiry and general slowness.

Login failures have been tricky to work out the source, as the only way to use the Fedora Zanata is through Fedora authentication. We will continue to look into this and we hope it will only get better.

Short authentication expiry has been a problem for a while and we will improve this in the next version of Zanata.

We are currently doing some fairly large changes under the hood of Zanata that should make a difference in an upcoming release.

### Command Line

The download size, installation process and general experience of using the command line client is something that needs to improve. There has been some more work on the Python client recently, and we hope to bring this back to feature parity with the Java client.

We recently make the client available to [install with 0install](http://zanata-client.readthedocs.org/en/latest/#installation) which simplifies the install process and shrinks the download size.

At the same time we are still adding new options to the CLI, so if there is something specific you would like to see, we'd love [more feedback](https://zanata.atlassian.net/secure/Dashboard.jspa).

### Right to Left Language Support

This isn't really excusable. [We will have this implemented](https://zanata.atlassian.net/browse/ZNTA-747) once we have a beta release of the new editor and then we will integrate it into the rest of the interface.

### Everything Else

- Clearer handling of versions
- Translation context enhancements
- Multiple translation file downloads
- Make comparing translations easier
- Current editor needs improvement on small screens (This works in the alpha editor)
- Better special character handling in editor
- Better plural support
- A way to translate, download, and upload entire groups, not just by project
- Possibly regular meetings with Zanata team to handle community questions (Monthly/Bi-monthly)
- Update/Newsletter style email to community about changes, improvements & fixes
- Better status updates on existing bugs/feedback in JIRA

## What is working

It was nice to get some positive feedback too. Here is some of the things you liked about Zanata:

### Good/Friendly/Clean UI

This was the most common feedback we received. There are some that disagree with this too, but the good news is, we hope the only change to this is to improve it. So we only plan on making the UI more friendly, clean, and usable.

### Open Source

This was expected, especially from a great open source community like Fedora. Thankfully, this won't be changing.

### Editor

This is an area we have always focused on and worked closely with translators to improve. Filtering, project-wide search and replace, and collaborative editing were some specifically mentioned features. There was some positive feedback about the new alpha editor too. If you want to see where the editor in Zanata is heading, have a look for yourself. It doesn't have all the features yet, but the more feedback the better.

### Other positive feedback

- Access to TM
- Continuous improvement
- Versions/branches in project
- Fedora authentication
- Credit references are updated when changing profile info

## In Conclusion

If you have anything you think we missed, you always report an issue or ask a question over on [our JIRA](https://zanata.atlassian.net/secure/Dashboard.jspa). You can find all our existing issues there too. If you see an existing issue you think needs more attention, vote it up or add any other comments you have.

We'd like to thank you all for helping us improve Zanata and therefore the Fedora translation community. As you can see we've taken on all this feedback and are working through it as best we can.

We look forward to working closely with you all in the future.
