---
title: Shared State
seo-title: Shared State in Adobe Launch
description: 
seo-description: 
---

# Shared State

**MODULE\_NAME**: `com.adobe.module.acquisition`

| **Key** | **Type** | **Description** |
| :--- | :--- | :--- |
| referrerdata | Map/Dictionary | Contains the referrer information. These information are optional and will be available in shared state map when they are provided to the SDK. **Push Message ClickSubKeyDescription**a.push.payloadIdthe id of push message which was clicked to open the app **LocalNotification/IAM Message ClickSubKeyDescription**a.message.idthe id of LocalNotification**/**IAM message which was clicked to open the appa.message.clickedclicked value is set to "1" **Deeplink DataSubKeyDescription**&lt;DeepLinkDataMap&gt;Contains the query parameters from the deferred deep link passed through the public AP **V3 AcquisitionSubKeyDescription**&lt;DataMap from the fingerprint server&gt;Combination of adobe data and context datalinkdeferredthe deferred deep link from the fingerprint server **Android : Google referrerDataSubKeyDescription**a.referrer.campaign.sourceThe "utm\_source", to identify the advertiser, site, publication, etc. that is sending traffic to your property, for example: google, newsletter4, billboarda.referrer.campaign.mediumThe "utm\_medium", the variable is used to track the advertising medium like email, Banner Ad or Pay per Click Adsa.referrer.campaign.termThe "utm\_term", the custom variable is used to tag paid keywords.a.referrer.campaign.contentThe "utm\_content", variable to differentiate similar content, or links within the same ada.referrer.campaign.nameThe "utm\_campaign", the variable used to track a campaign at a higher level.a.referrer.campaign.trackingcodeThe tracking code |

