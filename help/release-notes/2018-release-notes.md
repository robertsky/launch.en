---
title: 2018 release notes
seo-title: 2018 release notes for Adobe Launch
description: 2018 release notes for Adobe Launch
seo-description: 2018 release notes for Adobe Launch
---

# 2018 release notes

## November 14, 2018

### Features

#### Private extensions

Private extensions are now available! Private extensions are extensions that are developed by your company and are only available for properties within your own company. No one else can see or use them. Other than that, they behave exactly like regular extensions.

Would you like to provide a standard set of functionality that hundreds of your properties should use in the same way? Package that up into an extension and have all your properties use it. Writing the same custom code and using it over and over again? Put that into an extension and stop writing custom code.

#### Development properties

When you create properties, there is now an advanced option to "Configure for extension development". This creates a "Development" property that can be used for testing your private extensions during development before you're ready to make them available on your regular properties.

#### Rule Copy

You can now make a copy of a rule within the same property. Before you ask, the answer is "Yes, copying it to another property is coming next."

## November 8, 2018

### Updates

#### Core extension:

* **Persist Cohort option** The option to persist a cohort has been added to the Sampling condition. This has the effect of keeping a user in or out of the sample cohort across sessions. For example, if the “persist cohort” checkbox is checked and the condition returns true the first time it is run for a given visitor, it will return true on all subsequent runs of the condition for the same visitor. Similarly, if the “persist cohort” checkbox is checked and the condition returns false the first time it is run for a given visitor, it will return false on all subsequent runs of the condition for the same visitor.
* **Bug fix** Fixed an issue where a rule using a Page Bottom event and a Custom Code action on a page where Launch was being loaded synchronously but improperly installed (no call to `_satellite.pageBottom()`) would clear website content.
* **Bug fix** Fixed an issue where the Enters Viewport would not function if the Launch library was loaded asynchronously and finished loading after the browser's DOMContentLoaded event was fired.

### Bug fixes

* Fixed an issue where attempting to use scrollbars within some dropdowns would close the dropdown.
* Fixed an issue in Safari that prevented removing an item from a publishing library.
* Fixed an issue where some buttons in Launch extensions were not spaced properly.
* Fixed an issue where a rule using a Library Loaded event could not successfully trigger a separate rule (usually attempting to trigger a separate rule by using `_satellite.track()`).

## October 9, 2018

### Updates

* Conditions and exceptions have been combined in the rule builder, because order matters.  This more accurately reflects how they are treated within the system and at runtime. To make an exception, click the `Add` button under Conditions and choose Exception from the Logic Type selector.
* If you're using the Managed by Adobe host, older builds will now be cleaned up when new builds are published.
* There is now an icon next to the property name to indicate property type.

### Bug fixes

* When saving disabled resources in a library, there was a logical loop during the check for extension dependencies. That has been fixed.
* Org switcher now looks better on smaller screens.
* Certain build failure messages would fail to render.  Now they render.

## September 27, 2018

### Features

Launch has gone mobile!!

Used by thousands of customers for web tag management, Adobe Launch can now be used to manage your mobile SDKs.

Creating a mobile property in Launch allows you to:

* Create data elements and build sophisticated rules that can combine actions across multiple solutions.
* Manage mobile extensions:
  * Mobile Core and Profile extensions are pre-installed with every mobile property.
  * Extensions are available for other Adobe solutions including Adobe Analytics, Adobe Target and Adobe Audience Manager.
* Mobile Core extension and all additional extensions can be downloaded and installed through a dependency managers such as Maven and CocoaPods.
* When you add an extension, you must recompile your app and complete the app store submission/approval process.

  Data elements, rules, and extension configs are delivered to your application dynamically, are updated at app launch, and do not require app store updates.

For more information about getting started with mobile properties, see [Mobile](https://aep-sdks.gitbook.io/docs/).

## September 6, 2018

### Features

When you save a library, Launch will now check all the resources in it and prompt you to add any required extensions that are missing.

### Updates

1. Rights in the Admin Console have been slightly rearranged.  Manage Properties now belongs to the Company Rights group.  All other permissions (Manage Environments, Manage Extensions, Develop, Approve, and Publish) are in the Property Rights group.
1. Database improvements to improve API response times.

### Bug fixes

There were some edge cases where the rule builder would not display rule components in the same order that the database was saving them in. Now rule builder always displays rule component order correctly.

## August 23, 2018

### Features

Newly created Launch properties now come with a "Managed by Adobe" host and three environments (one of each type) by default.

## August 14, 2018

### Updates

The extension catalog is now sorted by display name rather than name.

### Bug fixes

* When switching properties, the cache was not clearing correctly and incorrect warnings displayed to users about which extensions were installed
* Rules with modified actions now correctly show as changes when adding to a library in all cases

## August 7, 2018

### Features

#### Extension upgrade

Launch users will now be notified when new versions of extensions are available and can install them on their own. Read more [here](../launch-reference/managing-resources/extensions/extension-upgrade.md).

### Updates

Embed codes have moved from the Environment detail page to an installation instructions modal. This modal is displayed automatically after you create a new environment and is accessible from the Environments List view.

## July 24, 2018

### Bug fixes

* In some scenarios, rules saved through the UI were not being saved with the correct order.  This has now been fixed.  In a future update, a data migration will fix all affected rules, but in the meantime manually editing the rule, making a change, and saving will fix an impacted rule.

## July 10, 2018

### Updates

* Anchor Delay has been moved from Property Settings to configuration for the Core extension Click event
* Tracking Cookie Name has been moved from Property Settings to the Adobe Analytics, Google Universal Analytics, and Cookie Optin condition settings

## May 24, 2018

### Features

#### Launch and DTM libraries are now live in China

The Launch and DTM libraries using Akamai are now available on CDN edge nodes in China. This provides much faster library load speeds for end users in China.

#### Improved error messages

The information contained in error messages has been improved and expanded throughout the API and UI. This should be especially useful for build failure messages.

#### Add All Changes button

Changed the behavior of the Add All Changes button on the Edit Library page. Previously, a resource was only considered "changed" until you had added it to a Library and saved it. Now a resource is considered "changed" until it has been published to the Production environment.

#### Adobe Privacy extension

The Adobe Privacy extension provides functionality for collecting and/or removing user IDs assigned to end users by Adobe solutions.

## May 8, 2018

### Features

#### Data Elements duration, "None" option

Data Elements now have a "None" duration option. Newly created Data Elements default to this setting.

#### Environment pages default to display async embed codes

Environment pages now display async embed codes as the default. Toggling between sync and async works exactly as before.

## May 3, 2018

### Documentation

Open source documentation for Launch now available at [https://docs.adobelaunch.com](https://docs.adobelaunch.com).

## April 24, 2018

### Enhancements

#### Rule builder

Events in rule builder are no longer draggable.

#### Extension delete

Improved warning messages.

### Bug fixes

* No longer prompt for unsaved changes on rule components when

  changes have been saved.

* Fixed problematic interactions with Active Library.

## April 17, 2018

### Features

#### Rule ID enhancement

Rule ID is now emitted for each rule in a build, and can be referenced in the browser.

#### Page Load event order

Page Load events now execute in logical order in async deployments (Library Loaded &gt; Page Bottom &gt; DOM Ready &gt; Window Loaded).

## April 11, 2018

### Features

#### Interface enhancements

Minor style improvements.

## April 3, 2018

### Features

#### Interface improvements

* Active Library has been moved to the top right to make more space for content
* Action buttons moved to the top right
* Bulk Edit now lists smarter actions, collapsed into a More menu on smaller screens
* Form fields now have default focus

## March 20, 2018

### Features

#### Exchange Link on Extension Cards (Support for future use)

Support was added to extension cards on the catalog page for future Learn More links to more information on the Extension Detail page on adobeexchange.com

#### Client-side enhancement

Event details are copied to the top-level event object (`%event.detail%` in text fields and `event.detail` in custom code)

## March 13, 2018

### Features

#### Delete resources

You can delete data elements, rules, and extensions. See [Delete Resources](../launch-reference/managing-resources/delete-resources.md).

#### Link DTM Embed Code to Launch

When you link your DTM embed code to Launch, you can keep your DTM production embed code on a page, but serve Launch files there instead of DTM. See [Link DTM Embed Code to Launch](2018-release-notes.md).

<!--The above link goes to this file-->

## March 6, 2018

### Enhancements

#### User interface changes

This release includes several interface enhancements:

* Rebranding of Marketing Cloud to Experience Cloud
* Element styling

### Bug fixes

Fixed an issue that caused a database query to take a long time to run and cause occasional 502 errors on API queries

## February 8, 2018

### Features

#### Active Library enhancements

* Enable/Disable actions ask if you want to add to your Active Library
* Create a new library from the Active Library drop down

## February 1, 2018

### Features

#### Akamai cache control headers

Cache control headers are now automatically set for libraries hosted on Akamai (assets.adobedtm.com). Previously, we did not set cache control headers for any files hosted on assets.adobedtm.com.

* Production builds: Cache control headers are set to 60 minutes
* Staging builds with "-staging" in the filename: Cache control headers are set to 0 minutes
* Dev builds with "-development" in the filename: Cache control headers are set to 0 minutes
* Launch Staging builds without "-staging" in the filename: The default of 60 minutes is inherited
* Launch Development builds without "-development" in the filename: The default of 60 minutes is inherited

>[!NOTE] It is up to browsers to receive and respect the cache control headers. Some browsers might ignore them.

>[!IMPORTANT] Launch developers who do not have `-development` or `-staging` in their Environment embed codes need to re-create their Development and Staging environments to get the 0 cache control header. If you don't re-create the environments, you'll have the same 60-minute cache control as the production libraries.

## January 18, 2018

### Features

#### Rule ordering {#rule-ordering}

Events in rules can now be assigned an order. When an event is triggered, any rules that use that event are executed in the order defined. Lower numbers run first (1 comes before 10). See [Rule ordering](2018-release-notes.md#rule-ordering) for more information.

<!-- The above link points to itself-->

#### Set active library

Set a new or existing library as your active library. When creating/editing rules, data elements, or extensions, you'll now have an option to save and build to your active library. This will immediately save your change to your library and execute a build. The status of the build can also be seen.

#### Multiple arguments in the logger

You can now pass actual objects to the log function and view them as objects in the browser console when using `_satellite.debug()`. This makes the Launch logger behave a lot more like console.log. To enable this change, there is no longer a persistent history attached to the `_satellite.debug()` function, so when you call it for the first time, you'll no longer see a history of past events. You will see any debug messages from that point forward.

## January 10, 2018

### Features

#### Asynchronous deploy of Launch

* On-page

  The Launch library now includes support for running asynchronously. There are important ramifications for how this changes what happens in your library. You should read the [Async documentation](../launch-reference/client-side-information/asynchronous-deployment.md) before you do anything.

* Async Toggle on Environments

  When retrieving the embed code for an environment, you can now flip a toggle switch to get the embed code if you want the library to load asynchronously.

#### User interface enhancements

* Information Videos on Empty List Pages
* Persistent filters

### Other changes

The following changes were made to be more descriptive of the actual behavior in sync and async scenarios:

* Page Top is now called Library Loaded
* On Load is now called Window Loaded

### Bug fixes and enhancements

* Fixed an issue where the Launch library would load twice in certain edge cases.
* There are now audit log entries for Property Delete.
* Improved the load speed of the Revision Selector when you quickly click from one entry to another.
* Help links now open in a new tab.

## Initial release

Release date: **November 8, 2017**

Important: Launch is being rolled out incrementally to Adobe Experience Cloud customers. If you have would like a chance to get early access, please put let us know by entering the required information in the Launch Release Form.

This is the first release of Launch.

Launch is the next-generation of tag management capabilities from Adobe. Launch gives customers a simple way to deploy and manage all of the analytics, marketing, and advertising tags necessary to power relevant customer experiences.

Launch empowers anyone to build and maintain their own integrations with Launch, called Extensions. These extensions are available to Launch customers in an app-store experience so they can quickly install, configure, and deploy their tags.

Launch enables you to:

Launch is offered to Adobe Experience Cloud customers as an included, value-add feature. Launch is an entirely new product with a new code base, designed to replace the previous Dynamic Tag Management (DTM) service. However, DTM will continue to be supported for the foreseeable future. Adobe will continue to fix any significant bugs and ensure consistent performance. At this time, no major feature enhancements are planned for legacy DTM.

### Key benefits

* Faster time to value
* Trustworthy data through centralized collection, organization, and delivery using data elements
* Compelling experiences through the integration of data and marketing technology using rule builder

### Key features

#### Extensions

An extension is a package of code (JavaScript, HTML, and CSS) that extends the Launch UI and client functionality. ​Build, manage, and update your integrations using a virtually self-service interface. You can think of Launch as an operating system, and extensions are the apps you use to achieve your tasks.

#### Extension catalog

Browse, configure, and deploy marketing/advertising tools built and maintained by independent software vendors.

#### Rule builder

Create robust rules that combine multiple events, sequenced in the way that you determine using if/then logic with conditions and exceptions. Extensions provide options for:

* Events
* Conditions
* Exceptions
* Actions

The rule builder includes real-time error checking and syntax highlighting for your custom code.

When the criteria outlined in your rules are met and conditions are satisfied, the actions you define are executed in order.

#### Data elements

Collect, organize, and deliver data across web-based marketing and advertising technology.

#### Enterprise publishing

The publishing process enables teams to publish code to pages. Different people can create an implementation, approve it, and publish it to your pages.

* Changes to your code are encapsulated within libraries you define ​
* You specify where and when you want your code deployed ​
* Multiple libraries can be built in parallel by different teams ​
* Unlimited development environments ​
* Deliberate, permissioned process for merging libraries together ​

#### Open APIs

Automate implementations of individual technologies, or a group of technologies.

* Launch interacts with the Reactor APIs ​
* Deployments can be automated through APIs ​
* Integrate the Launch APIs with your own internal systems ​
* You can build your own user interface, if desired ​

#### Light, modular container tag

The Launch container tag is 60% lighter than Adobe Tag Manager and 40% lighter than Google Tag Manager. The content of your container is minified, including your custom code. Everything is modular. If you don't need an item, it is not included in your library. The result is an implementation that is fast and compact.

## Other highlights

Launch provides several improvements over similar systems, including:

* No use of `document.write ()` where Chrome doesn't allow it ​
* The Page Top and Page Bottom rules are bundled into the main library to minimize unnecessary HTTP calls ​ ​
* Custom action scripts within a rule can be loaded in parallel, but are executed sequentially ​
* If you avoid Page Top and Page Bottom rules, the code is mostly asynchronous, with a path to getting fully async ​
