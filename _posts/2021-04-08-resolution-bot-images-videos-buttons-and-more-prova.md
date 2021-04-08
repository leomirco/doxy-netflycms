---
layout: post
title: "Resolution bot: images, videos, buttons and more prova"
date: 2021-04-08T13:24:40.298Z
featured: false
draft: false
comment: false
excerpt: "Resolution bot: images, videos, buttons and more"
post_image: /images/uploads/service-icon3.png
autore: Ilenia
categories: chatbots
tags:
  - functionality
  - Resolution bot
  - Configuration
---
![Resolution bot: images, videos, buttons ](/images/uploads/dialogflow-microlanguage-v2.png "Resolution bot: images, videos, buttons ")

## Introduction

Tiledesk widget (web and mobile) supports many special messages that go beyond simple text.

A chatbot can reply for example with images, videos or a message with button replies. We designed **Microlanguage** exactly for this kind of task. Microlanguage is a language made of simple “tags” that make it simple to use feature-rich messages in your chatbot. You can use Microlanguage with Tiledesk Dialogflow native chatbot, all Tiledesk chatbots and the External chatbots that you connect to Tiledesk itself.

## When using Tiledesk Microlanguage

You can generally use Microlanguage to increase the end-user experience, i.e. proposing to your customers to reply using a buttons, or sending them images or videos or to handoff the conversation to human agents.

## Microlanguage for Response bot

Microlanguage is a set of special text commands (simple tags) that you can easily embed into your Response bot.

For example, if you want to send an image to Tiledesk widget you can write a Answer like the following:

*Hello, this is ietf.org logo* 

*tdImage:https://www.ietf.org/media/images/ietf-logo.original.png*

You will get on the Tiledesk Widget:

![image to Tiledesk widget ](/images/uploads/100596624-ac5f3480-32fc-11eb-9c15-1160d7d85204.png "image to Tiledesk widget ")

## Supported commands

Here follows a list of the supported microlanguage tags.

## Send text

To send text you can simply write your message in the Response:

![your message in the Response](/images/uploads/100437816-9b66b700-30a1-11eb-8c1b-7ffbcd4940f8.png "your message in the Response")

And the message will be rendered on the Widget in the chatbot reply balloon:

![the message will be rendered on the Widget](/images/uploads/100438803-f8af3800-30a2-11eb-93af-afc0cd457fc0.png "the message will be rendered on the Widget")

## Send images

Tag: *tdImage*

Send an image with *tdImage:IMAGE_URL* tag in your response text:

![Send an image with *tdImage*](/images/uploads/100603390-517e0b00-3305-11eb-8bba-2de6d90ff085.png "Send an image with *tdImage*")

Use of **tdImage** tag

It will be rendered on the user widget as an image followed by the optional text part:

![tdImage tag](/images/uploads/100440948-f6021200-30a5-11eb-953b-c0937f46a62f.png "tdImage tag")

Users will see the image in place of the link

### tdImage – Syntax

This tag MUST be placed on the start of a newline.

*tdImage:IMAGE_URL*

Specify optional text simply adding one or more lines of text:

Here you have the IETF official logo: 

*tdImage:https://www.ietf.org/media/images/ietf-logo.original.png*

Example:

Use the logo to spread Internet technology! 

*tdImage:https://www.ietf.org/media/images/ietf-logo.original.png*

#### Specify image size (Optional)

tdImage,wWIDTH hHEIGHT:IMAGE_URL

Example:

*tdImage,w100 h100:https://www.ietf.org/media/images/ietf-logo.original.png*

## Text Buttons

Syntax: Use ‘*’ followed by one space, then the button’s text (must start on a new line of the answer text)

Sometimes you want to allow end-users to easily reply using Buttons. You can achieve this task with buttons, providing fast replies to your chatbots. With Microlanguage you can use the special Button syntax to render a button, like this:

![Text Buttons](/images/uploads/102228233-c26b1880-3eea-11eb-818d-8ee3a32adc5a.png "Text Buttons")

This will be rendered on the user widget as a couple of buttons.

**When the user presses the button the widget simply sends the button’s text back to the chatbot**.

![Text Buttons](/images/uploads/102227963-74eeab80-3eea-11eb-8df0-c6ccc16c23ce.png "Text Buttons")

Generally *\*reply buttons\** are embedded in chatbots replies. Reply buttons allow users to reply with a proposed sentence already built by the sender (generally the chatbot). Pressing the button simply sends the sentence (the text contained in the button) to the recipient (most of the time the external chatbot) on the other side.

### Buttons – Syntax

With Microlanguage you can render a button with a syntax similar to the one used to render “Unordered Lists” in *Markdown*. With the markdown unordered list syntax, you will render a button on the native Tiledesk widget.

Example:

*Are you sure?* 

*\* Yes* 

*\* No*

## Link Buttons

You can use buttons also as an alternative to links in messages. While Tiledesk widget always renders http URLs found in the message, sometimes it is more feasible to show a big button to power the link importance and his accessibility.

With Microlanguage you can alway use the basic Button syntax, that renders a button, with the addition of a URL placed right after the button text. This will render a special button, with a small arrow on the top right corner, that indicates it as a link. Look at this example:

![Link Buttons](/images/uploads/102229451-1fb39980-3eec-11eb-8c7a-8ba17ebcd6cf.png "Link Buttons")

It will be rendered on the user widget as:

![Link Buttons](/images/uploads/102229349-fa269000-3eeb-11eb-93c5-0647b982a6c5.png "Link Buttons")

Pressing the button will open the link in another another browser tab.

### Link Button – Syntax

Place this tag on a Button line, just after the button text.

*Link Button syntax:* 

*\* Button text HTTP-URL*

Example:

*Choose your pricing* 

*\* Cloud https://tiledesk.com/pricing-cloud/* 

*\* Self-managed https://tiledesk.com/pricing-self-managed/*

#### Link Button – Specify the link’s target window (Optional)

You can specify if the target is another page or the same page where the widget is hosted. Default Links will open the specified URL in another tab/window of the browser. If you want to open the URL in the same widget’s page use a parent instead, separating the URL by two spaces instead of just 1, from the last button word:

*Tiledesk website:* 

*\* Go to Tiledesk https://tiledesk.com*

**NOTE**: There are 2 spaces between ‘Tiledesk’ and ‘[http://tiledesk.com](http://tiledesk.com/)‘.

## **Action Buttons**

You can use Action Buttons to allow custom communication to your chatbots. This means that you will not send to the remote chatbot webapp the button’s text but rather a hidden code (the action value) that identifies a specific action on the backend. You can use this kind of buttons to communicate some special action to the chatbot that not always depends by the text embedded in the button.

With Microlanguage you always use the basic Button syntax, that renders a button, with the additional option **tdAction:ACTION-NAME**, placed right after the button text. This will render a special button that, when pressed, shows a special animation that indicates it as an “Action” button.

### tdAction – Syntax

This tag MUST be placed on the start of a newline.

Action button syntax:

*\* BUTTON TEXT tdAction:SPECIAL-ACTION*

Example:

*Vote for your president* 

*\* Trump tdAction:VOTE-TRUMP* 

*\* Biden tdAction:VOTE-BIDEN*

**tdActionShowReply (Optional)**

Default Action Button doesn’t show any text as “sent”. It simply “flashes”. If you want to send effectively a text (and the action) to your chatbot you can use the tdActionShowReply option (instead of tdAction) to effectively send the button text to your chatbot

*\* BUTTON_TEXT tdActionShowReply:ACTION-CALLBACK-NAME*

## Frame

Tag: *tdFrame*

Send a web content embedded into an iframe with *tdFrame:PAGE_URL* tag in your response text:

This tag works just like the tdImage but instead of an image it will send to the widget am iframe with a page content in a box. You can also specify the box size, as you do with tdImage tag. This tag is extremely useful if you want to send to the user pluggable components not supported by the widget as **calendars**, **web maps**, **mini games** etc.

For example, write this:

![Frame](/images/uploads/100668900-ea8c4080-335c-11eb-9556-e65f61983143.png "Frame")

This sends a minigame embedded in an iframe

To play this inline mini game directly in the widget!

![Frame](/images/uploads/100668715-a5680e80-335c-11eb-95f5-f91528209cff.png "Frame")

That you can play in the widget!

### tdFrame – Syntax

This tag MUST be placed on the start of a newline

*tdFrame:FRAME_URL*

Specify optional text simply adding one or more lines of text:

*Here you have some text:* 

*tdFrame:https://www.emanueleferonato.com/wp-content/uploads/2019/02/runner/*

### tdFrame – Example: send a map

To send a google map simply write a text reply like this:

*This is the address* 

*tdFrame:https://www.google.com/maps/embed?*

*origin=mfe&pb=!1m3!2m1!1suniversity+of+san+francisco!6i13*

You will get a map rendered in the widget:

![tdFrame](/images/uploads/100669528-d1d05a80-335d-11eb-9e81-2721ea55a033.png "tdFrame")

A Google Map sent by the Dialogflow agent is rendered in the Tiledesk widget

#### Frame size (Optional)

tdFrame,wWIDTH hHEIGHT:FRAME_URL

*Small map example*:

Write *tdFrame,w150 h150* to reduce the size of the map:

*This is the address* 

*tdFrame,w150 h150:https://www.google.com/maps/embed?origin=mfe&pb=!1m3!2m1!1suniversity+of+san+francisco!6i13*

You will get a smaller map frame:

![Frame](/images/uploads/100669905-6044dc00-335e-11eb-93c3-390df3b694b9.png "Frame")

## Video

Tag: *tdVideo*

With this tag the chatbot can send mp4 or Youtube videos to the user.

### tdVideo – Syntax

This tag MUST be placed on the start of a newline.

*tdVideo:VIDEO_URL*

Specify optional text simply adding one or more lines of text:

*Here you have some text:* 

*tdVideo:https://file-examples-com.github.io/uploads/2017/04/file_example_MP4_480_1_5MG.mp4*

### tdVideo – Example: send MP4 video

Write a text reply like this:

*Your video here* 

*tdVideo:https://file-examples-com.github.io/uploads/2017/04/file_example_MP4_480_1_5MG.mp4*

The video will be rendered in the widget like this:

![video](/images/uploads/101215094-782da000-367d-11eb-93ca-57dbd11df5c9.png "video")

## Handoff to human agents

Sometimes, during a conversation with your Dialogflow agent, you want the user to opt for a switch to a human agent.

With *Microlanguage* this is a very easy task. Just add the \agent tag on a new line at the end of the text reply.

Tag: *\agent*

With this tag the chatbot will remove the current chatbot (the Dialogflow agent) from the corresponding conversation and will try to invite a human, following the current department rules. If no agents are available the conversation will wait in the “unserved” queue until an agent becomes available again.

### \agent – Syntax

Add the **\agent** tag on a new line at the end of the text reply, as in the following example:

*We are putting you in touch with an operator* 

*\agent*

In Dialogflow you can train an specific intent to switch to humans, as in the following example:

![Talk to agent](/images/uploads/79358037-07e0db80-7f41-11ea-8d3b-ea4064ea2edf1.png "Talk to agent")

The **\agent** keyword, at the end of the reply phrase, will never be shown to the *end-user* and will be removed from the reply text. It is an instruction for Tiledesk to switch the conversation to humans. As soon as Tiledesk see this instruction in the text it will remove the current chatbot (the Dialogflow agent) from the corresponding conversation and will try to invite a human, following the current department rules. If no agents are available the conversation will wait in the “unserved” queue until an agent becomes available again.

Do you have feedback on this article? Please send us your feedback writing an email to [info@tiledesk.com](mailto:info@tiledesk.com)