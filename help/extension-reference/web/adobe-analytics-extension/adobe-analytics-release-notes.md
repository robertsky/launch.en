---
title: Adobe Analytics Release Notes
seo-title: Adobe Analytics Release Notes for Adobe Launch
description: Adobe Analytics Release Notes for Adobe Launch
seo-description: Adobe Analytics Release Notes for Adobe Launch
---

# Adobe Analytics Release Notes

## April 15, 2019

### Adobe Analytics Extension 1.7.4

#### Bug Fixes

* Rolled extension back after a bug was found in appMeasurement 2.13.0. appMeasurement 2.13.0 was causing an issue that wasn't sending the ECID, so if you installed 1.7.3 we recommend upgrading to 1.7.4 to avoid this problem. Note that the clearVars will continue until an updated version of appMeasurement is released.

## April 12, 2019

### Adobe Analytics Extension 1.7.3

#### Bug Fixes

* Updated the Adobe Analytics Extension to appMeasurement 2.13.0 which includes a fix to a known clearVars issue.

## March 21, 2019

### Adobe Analytics Extension 1.7.2

#### Features

* Updated the Adobe Analytics extension to DIL 9.1.
* Updated the Adobe Analytics extension to appMeasurement 2.12.
* Upgraded the Adobe Analytics extension view to React-Spectrum.
* When configuring your report suites in the configuration page you will now see a dropdown to all of the report suites in your company to make it easier for you to select the appropriate report suite.

## March 7, 2019

### Adobe Analytics Extension 1.7.1

#### Bug Fixes

* Rolled back the extension to version 1.6 after a bug was found in 1.7.

## February 11, 2019

### Adobe Analytics Extension 1.6

#### Features

* Updated the Adobe Analytics extension to DIL 9.0 which will support opt-in.
* Updated the Adobe Analytics extension to AppMeasurement 2.11 to support opt-in.

#### Bug fixes

* Fixed a conflict with Prototype JS. The Analytics extension will now support standard prototype.js libraries.

## November 9, 2018

### Adobe Analytics Extension 1.5.1

#### **Bug fixes**

* Downgraded the DIL module to 7.0 to fix an issue that was causing problems with analytics beacons not firing

## November 5, 2018

### Adobe Analytics Extension 1.5

#### **Features**

* Updated the Adobe Analytics extension to support DIL 8.0 in Audience Manager
* Separated the "Serialize from value" field into two, "Event ID" and "Event Value". This will fix the issue that was assigning a value instead of serializing an event
  * Please note: if you are using the current field to add an ID by using a string (ex. Event7=3:abc123) you will need to update your input to reflect the ID in the "Event ID" field

#### **Bug fixes**

* Fixed a bug that wasn't allowing the currency code to populate correctly

## October 11, 2018

### Adobe Analytics Extension 1.4

#### **Features**

* Migrated the tracking cookie name to the extension configuration.

#### **Bug Fixes**

* Fixed a bug so set variables don't crash when no trackerProperties object is available.

## June 5, 2018

### Adobe Analytics Extension 1.3

#### **Features**

* Updated Adobe Analytics extension to support [AppMeasurement 2.9](https://marketing.adobe.com/resources/help/en_US/sc/appmeasurement/release/c_release_notes_mjs.html).
* Added "Make tracker globally accessible" feature in the Adobe Analytics extension, which enables the tracker to be scoped globally under `windows.s`.

#### **Bug Fixes**

* Fixed a bug that caused list view to reset when returning from detail view
* Fixed a few bugs to improve loading of resources in the revision selector
* Fixed a bug where multiple rules were overwriting s.events in the Adobe Analytics extension

## March 20, 2018

### Adobe Analytics Extension 1.2

#### **Features**

* Updates AppMeasurement.js to 2.8.0
* Adds support for server-side forwarding

## February 8, 2018

### Adobe Analytics Extension 1.1

#### **Features**

* AppMeasurement has been updated to version 2.6
* The initialized Analytics tracker is now exposed through a shared module in the Launch extension so other extensions can include code to interact with it.

#### **Bug fixes**

* Fixed an error in the Adobe Analytics Extension that caused "Error, missing Report Suite ID in AppMeasurement initialization" to appear in the browser console.
