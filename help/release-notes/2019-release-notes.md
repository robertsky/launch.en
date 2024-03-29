---
title: 2019 release notes
seo-title: 2019 release notes for Adobe Launch
description: 2019 release notes for Adobe Launch
seo-description: 2019 release notes for Adobe Launch
---

# 2019 release notes

## May 8, 2019

The Reactor API that powers Launch is officially reaching 1.0 status today.  This comes with a commitment to maintaining backwards compatibility within this major version (the 1.x series).  To get started working with the Reactor API, please visit [https://developer.adobelaunch.com/api/\#](https://developer.adobelaunch.com/api/#).

### Updates

* A number of API changes have been made for this 1.0 release.  API release notes will be posted with the API documentation at [https://developer.adobelaunch.com/api/release\_notes/2019-release-notes/](https://developer.adobelaunch.com/api/release_notes/2019-release-notes/).
* `Adapter` has been renamed to `Host`. Audit events will contain the following items related to this change.
  * For each Adapter, you'll see a `Host.created` event.
  * For each Environment, you'll see an `Environment.updated` event to remove the relationship with the Adapter and add the relationship to the Host.
  * For each adapter, you'll see an `Adapter.deleted` event.

### Bug Fixes

* Fixed some inconsistencies with the Regular Expression tester used by various extensions.

## April 8, 2019

### Bug Fixes

* Improved a few build error messages
* Better reporting for failed SFTP Hosts

### Other

* Updated the way that Rule Components and Data Elements relate to extensions.  When you delete an extension and reinstall an extension, you no longer have to manually update your resources to point to the newly installed extension.
* Rule Components are now under Property instead of Rule.  This lays a foundation for future enhancements to Rule Components.

## March 20, 2019

### Updates

* Visual updates to the resource copy tool, including status indicators and a cancel button.

## March 5, 2019

### Bug Fixes

* Builds stored on Akamai will use a new folder structure.  Embed codes do not change. This will mediate many issues we've seen with builds to Akamai.

## February 20, 2019

### Updates

* Support for custom code has been added to Compare View.

### Bug fixes

* The cross-property workflow is now a bit smoother.

## February 12, 2019

### Features

* Cross-property Copy - You can now copy resources from one property to another.  After selecting a resource and clicking the **Copy** button, you can select a target property to copy to.  This is available on Extensions, Data elements, and Rules.  Read more about copying resources [here](../launch-reference/managing-resources/copying-resources.md).

## January 29, 2019

### Features

* Revision Compare - You can now compare one version of a resource with older versions.  This is available on Extensions, Data Elements, and Rules.  Read more about this new feature [here](../launch-reference/managing-resources/compare-resource-revisions.md).

## January 17, 2019

### Updates

* Builds should be running ~15% faster than before.  Large builds (hundreds of resources) will have more dramatic improvements.

## January 8, 2019

### Core Extension 1.4.2

* The `Enters Viewport` event is now configurable to trigger each time that the element enters the viewport instead of just the first time.
* Custom Events can now contain extra contextual data that can be used in conditions and actions.
* Link Delay on the Click event will now trigger on descendants of the anchor and not just the anchor itself.

### Updates

* Properties that are configured for Extension Development now have a small tag next to the Property Name.
* OrgID is now available on the \_satellite object.
* Use of the Launch UI is no longer supported in IE11, you'll receive a warning if you login with IE 11.

### Bug fixes

* Better support for long Library names in your Active Library and the Publishing view.
* In certain scenarios, when you saved a library, the dependency checker would prompt you to add a new revision of an extension that was already in your Library. It doesn't do that anymore.
* Tooltips will now reliably show up in Safari.
* Searches in the search bar will now trigger a bit faster than before.
