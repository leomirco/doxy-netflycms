---
layout: post
title: "Resolution bot: images, videos, buttons and more"
date: 2021-04-07T15:56:24.074Z
featured: false
draft: false
comment: false
excerpt: "Resolution bot: images, videos, buttons and more"
post_image: /images/uploads/service-icon3.png
autore: Ilenia
categories: chatbot
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

*tdImage,wWIDTH hHEIGHT:IMAGE_URL*