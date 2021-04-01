---
layout: post
title: Getting started with Triggers
date: 2021-04-01T16:18:58.827Z
featured: false
draft: false
comment: false
excerpt: Getting started with Triggers
post_image: /images/uploads/service-icon3.png
autore: Ilenia
categories: getting_started_for_admins
tags:
  - functionality
  - Triggers
---
Here is where all automation happensWith triggers you can execute custom actions based on events triggered by the platform, all without programming skills.

System events are available, but custom events can be used too, and correspondent actions can be fired, through the Triggers dedicated panel.
 
For example:
• \[event] User opens a conversation
• \[event] Department is pre-served by a bot.
• \[Action] action “send hidden message to the bot”

Tiledesk comes with a set of default triggers already set up in your project. You can use these triggers as they are or modify them.
By default, some of these built-in Chat triggers are disabled on your project. If you would like to use one, simply click into the trigger, make any customizations you need to, and switch the Trigger status to Enabled. Don’t for get to Save changes.

The default triggers that come with your project are:

Online Welcome Greeting
Send a welcome message if there are online agents to the visitor that create a chat.

Checkout Page
The Checkout Page trigger is more of a skeleton to get you started than a ready-to-go trigger. It is designed as an example for Tiledesk customers who work in the world of retail, but it can also be adapted for other purposes. As is, this trigger is designed to reduce cart abandonment by engaging customers that are visiting on the checkout page.

Offline Welcome Greeting
Send a welcome message if there aren’t online agents to the visitor that create a chat.

Office Closed Notice
Send an office closed message if a visitor asks for support outside of the operating hours.

Invite Bot
Invite if available the department bot to the temporary chat and start it.

New Conversation
Create a temporary chat when new conversation button is pressed.

Creating Chat triggers

Chat triggers are created on the dashboard.

In the example below, we’re creating a trigger that sends a welcome message to users visiting your website:﻿

![creating a trigger that sends a welcome message to users ](/images/uploads/image-13.png "creating a trigger that sends a welcome message to users ")





### To create a trigger

From the dashboard, select Settings > Triggers.

1. Click **Add trigger**.
2. Enter a **name** and brief **description** for your trigger.
3. Click **Enabled** at the top to enable your trigger.
4. In the Customize Trigger section, use the Run trigger drop-down to select one of the following events that should fire the trigger:

   1. Select **When a visitor requests a chat** if you want the trigger to run when the visitor has requested a chat.
   2. Select **When a chat message is sent** if you want the trigger to run when the visitor has entered and sent text in the chat widget.
5. Under Check conditions:

   1. Select **Check all of the following conditions** if you want every condition you create to be met before the trigger is fired.
   2. Select **Check any of the following conditions** if you want one or more of the conditions you create to be met before the trigger is fired.
6. Select actions under Perform the following **actions**.
7. Click **Create** **triggers**.
8. When the trigger is created and enabled, a check mark appears in the Enabled column on the Triggers settings page.

Note: If you have multiple triggers that must be executed in a certain order, you need to add at least one second of wait time between each trigger. This is required due to the fact that triggers do not run in a particular order and are evaluated and executed simultaneously.

## Disabling Chat triggers

If you want a trigger to stop running, but do not want to delete it, you can simply disable it. Disabled triggers can be re-enabled at any time.

### To disable a trigger

1. From the dashboard, click **Settings** > **Triggers**, then click the trigger you want to disable.
2. In the Trigger status section, click **Disabled**.
3. At the bottom of the page, click **Save** **changes**. On the Triggers settings page, the check mark is removed from the Enabled column.
4. To re-enable a disabled trigger, click the trigger you want to enable, then click Enabled.

## Deleting Chat triggers

If needed, you can also delete triggers from the Triggers settings page. Deleted triggers cannot be recovered.

### To delete a trigger

1. From the Chat dashboard, click **Settings** > **Triggers**.
2. Click the **button** to the **left** of the trigger you want to delete
3. Confirm that you want to delete the trigger. The trigger is removed from the Triggers list.