---
title: Publishing
seo-title: Publishing in Adobe Launch
description: Publishing in Adobe Launch
seo-description: Publishing in Adobe Launch
---

# Publishing

This section contains information to help you understand the publishing process for Web extensions.

For an introductory video, see [Publishing workflow](https://www.youtube.com/embed/Pe-YSn26_xI).

There are a few components and relationships that are important to understand in order to take full advantage of the publishing workflow. These are:

* [Libraries](libraries.md)

  A library is a set of instructions for how extensions, data elements, and rules will interact with one another and with your website. Libraries are compiled into builds. A library can contain as many changes as you are comfortable making or testing at once.

* [Builds](builds.md)

  A build is the actual set of files containing the code that is delivered to each user's browser when that user views your site.

* [Environments](environments.md)

  An environment is a set of deployment instructions that tells Launch what format you'd like your build in and where you'd like that build delivered.

* [Hosts](hosts.md)

  A host represents the connection details for the environment to deliver the build. You can choose to let Launch manage the hosting of your build, or you can provide information for your own host servers.

* [Client-side code](../upgrade-from-dtm-to-launch/link-dtm-embed-code.md)

  The client-side code is the set of script code that you place on your site or in your application. This code tells each client device where to retrieve the build. The code is attached to an environment and can change when you make changes to your environment configuration.

The publishing process consists of:

1. Creating and editing libraries.
1. Testing the functionality of those libraries where you need to test them.
1. Deploying those libraries to your production environment.

![](/help/assets/publishing.jpg)

For example, if you create a new checkout event, create a revenue data element related to that event, and make a change to the Adobe Analytics extension configuration to support the new event and data element, you can save them all at once to a checkout library, then test, approve, and publish them as a group.
