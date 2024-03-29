---
title: Experience Cloud ID Service Extension
seo-title: Experience Cloud ID Service Extension for Adobe Launch
description: Information about configuring the Experience Cloud ID extension, and the options available when using this extension to build a rule
seo-description: Experience Cloud ID Service Extension for Adobe Launch
---

# Experience Cloud ID Service Extension

Use this reference for information about configuring the Experience Cloud ID extension, and the options available when using this extension to build a rule.

Use this extension to integrate the Experience Cloud ID Service with your property. With the Experience Cloud ID Service, you can create and store unique and persistent identifiers for your site visitors.

The ECID JS library can be found at this location: [https://github.com/Adobe-Marketing-Cloud/id-service/releases](https://github.com/Adobe-Marketing-Cloud/id-service/releases).

## Configure the Experience Cloud ID extension

This section provides a reference for the options available when configuring the Experience Cloud ID extension.

If the Experience Cloud ID extension is not yet installed, open your property, then click **[!UICONTROL Extensions &gt; Catalog]**, hover over the Experience Cloud ID extension, and click **[!UICONTROL Install]**.

To configure the extension, open the [!UICONTROL Extensions] tab, hover over the extension, and then click **[!UICONTROL Configure]**.

![](/help/assets/ext-mcid-config.png)

The following configuration options are available:

### Experience Cloud Organization ID

The ID for your Experience Cloud Organization.

Your ID is a 24-character, alphanumeric string followed by `@AdobeOrg`. If you do not know this ID, contact Customer Care.

### Exclude specific paths

The Experience Cloud ID does not load if the URL matches any of the specified paths.

(Optional) Enable Regex if this is a regular expression.

Click **[!UICONTROL Add]** to exclude another path.

### Variables

Set name-value pairs as Experience Cloud ID instance properties. Use the drop-down to select a variable, then type or select a value. For information about each variable, refer to the [Experience Cloud ID Service documentation](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-overview.html).

## Experience Cloud ID extension action types

This section describes the action types available in the Experience Cloud ID extension.

### Action Types

#### Set Customer IDs

Set one or more customer IDs.

1. Enter the integration code.

   The integration code should contain the value set up as a data source in Audience Manager or Customer Attributes.

1. Select a value.

   The value should be a user ID. Data elements are most suitable for dynamic values like IDs from a client-specific internal system.

1. Select an authentication state.

   Available options are:

   * Unknown
   * Authenticated
   * Logged out

1. (Optional) Click **[!UICONTROL Add]** to set more customer IDs.
1. Click **[!UICONTROL Keep Changes]**.
