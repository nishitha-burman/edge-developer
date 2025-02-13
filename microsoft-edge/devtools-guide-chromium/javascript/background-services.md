---
title: Debug background services
description: How to debug Background Fetch, Background Sync, Notifications, and Push Messages with Microsoft Edge DevTools.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: conceptual
ms.prod: microsoft-edge
ms.date: 05/04/2021
---
<!-- Copyright Kayce Basques

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->
# Debug background services

The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user doesn't have your website open.  A background service is functionally similar to a [background process](https://en.wikipedia.org/wiki/Background_process).

Microsoft Edge DevTools considers each of the following APIs to be a background service:

*  [Background Fetch](#background-fetch)
*  [Background Sync](#background-sync)
*  [Notifications](#notifications)
*  [Push Messages](#push-messages)

Microsoft Edge DevTools may log background service events for 3 days, even when DevTools isn't open.  The background service events log can help you make sure that events are being sent and received as expected.  You can also inspect the details of each event.

:::image type="content" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="The Push Messaging pane." lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::


<!-- ====================================================================== -->
## Background Fetch

The **Background Fetch API** enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.  To log Background Fetch event for 3 days, even when DevTools isn't open:

<!--Todo: add background fetch api section when available -->

1. To open DevTools, right-click the webpage, and then select **Inspect**.  Or, press `Ctrl`+`Shift`+`I` (Windows, Linux) or `Command`+`Option`+`I` (macOS).  DevTools opens.

1. In DevTools, on the main toolbar, select the **Application** tab.  If that tab isn't visible, click the **More tabs** (![More tabs icon.](../media/more-tabs-icon-light-theme.png)) button, or else the **More Tools** (![More Tools icon.](../media/more-tools-icon-light-theme.png)) button.

1. On the left, in the **Background Services** section, select **Background Fetch**.  The **Background Fetch** page opens.

   :::image type="content" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="The Background Fetch panel." lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::

1. Click **Record** (![Record.](../media/record-icon.msft.png)).
   After triggering some Background Fetch activity, DevTools logs the events to the table.

   :::image type="content" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="A log of events in the Background Fetch panel." lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::

1. Click an event to view its details in the space below the table.

   :::image type="content" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="View the details of an event in the Background Fetch pane." lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::


<!-- ====================================================================== -->
## Background Sync

The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.  To log Background Sync events for 3 days, even when DevTools isn't open:

<!--Todo: add background sync api section when available -->

1. To open DevTools, right-click the webpage, and then select **Inspect**.  Or, press `Ctrl`+`Shift`+`I` (Windows, Linux) or `Command`+`Option`+`I` (macOS).  DevTools opens.

1. In DevTools, on the main toolbar, select the **Application** tab.  If that tab isn't visible, click the **More tabs** (![More tabs icon.](../media/more-tabs-icon-light-theme.png)) button, or else the **More Tools** (![More Tools icon.](../media/more-tools-icon-light-theme.png)) button.

1. On the left, in the **Background Services** section, select **Background Sync**.  The **Background Sync** page opens.

   :::image type="content" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="The Background Sync pane." lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::

1. Click **Record** (![Record.](../media/record-icon.msft.png)).  After triggering some Background Sync activity, DevTools logs the events to the table.

   :::image type="content" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="A log of events in the Background Sync pane." lightbox="../media/javascript-application-background-services-background-sync.msft.png":::

1. Select an event to view its details in the space below the table.

   :::image type="content" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="View the details of an event in the Background Sync pane." lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::


<!-- ====================================================================== -->
## Notifications

After a **service worker** has received a [Push Message](https://developer.mozilla.org/docs/Web/API/Push_API) from a server, the service worker uses the [Notifications API](https://developer.mozilla.org/docs/Web/API/Notifications_API) to display the data to a user.  To log Notifications for 3 days, even when DevTools isn't open:

1. To open DevTools, right-click the webpage, and then select **Inspect**.  Or, press `Ctrl`+`Shift`+`I` (Windows, Linux) or `Command`+`Option`+`I` (macOS).  DevTools opens.

1. In DevTools, on the main toolbar, select the **Application** tab.  If that tab isn't visible, click the **More tabs** (![More tabs icon.](../media/more-tabs-icon-light-theme.png)) button, or else the **More Tools** (![More Tools icon.](../media/more-tools-icon-light-theme.png)) button.

1. On the left, in the **Background Services** section, select **Notifications**.  The **Notifications** page opens.

   :::image type="content" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="The Notifications pane." lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::

1. Click **Record** (![Record.](../media/record-icon.msft.png)).  After triggering some Notifications activity, DevTools logs the events to the table.

   :::image type="content" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="A log of events in the Notifications pane." lightbox="../media/javascript-application-background-services-notifications.msft.png":::

1. Click an event to view its details in the space below the table.

   :::image type="content" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="View the details of an event in the Notifications pane." lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::


<!-- ====================================================================== -->
## Push Messages

To display a push notification to a user, a **service worker** must first use the [Push Message API](https://developer.mozilla.org/docs/Web/API/Push_API) to receive data from a server.  When the service worker is ready to display the notification, it uses the [Notifications API](https://developer.mozilla.org/docs/Web/API/Notifications_API).  To log Push Messages for 3 days, even when DevTools isn't open:

1. To open DevTools, right-click the webpage, and then select **Inspect**.  Or, press `Ctrl`+`Shift`+`I` (Windows, Linux) or `Command`+`Option`+`I` (macOS).  DevTools opens.

1. In DevTools, on the main toolbar, select the **Application** tab.  If that tab isn't visible, click the **More tabs** (![More tabs icon.](../media/more-tabs-icon-light-theme.png)) button, or else the **More Tools** (![More Tools icon.](../media/more-tools-icon-light-theme.png)) button.

1. On the left, in the **Background Services** section, select **Push Messaging**.  The **Push Messaging** page opens.

   :::image type="content" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Open the Push Messaging pane." lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::

1. Click **Record** (![Record.](../media/record-icon.msft.png)).  After triggering some Push Message activity, DevTools logs the events to the table.

   :::image type="content" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="A log of events in the Push Messaging pane." lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::

1. Click an event to view the details in the space below the table.

   :::image type="content" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="View the details of an event in the Push Messaging pane." lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::


<!-- ====================================================================== -->
> [!NOTE]
> Portions of this page are modifications based on work created and [shared by Google](https://developers.google.com/terms/site-policies) and used according to terms described in the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0).
> The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques](https://developers.google.com/web/resources/contributors#kayce-basques) (Technical Writer, Chrome DevTools \& Lighthouse).
[![Creative Commons License.](https://i.creativecommons.org/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0)
This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0).
