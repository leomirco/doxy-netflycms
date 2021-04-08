---
layout: post
title: Handoff to human agents
date: 2021-04-07T15:29:31.126Z
featured: false
draft: false
comment: false
excerpt: Handoff to human agents
post_image: /images/uploads/service-icon3.png
autore: Andrea
categories: chatbots
tags:
  - functionality
  - human agent
  - Resolution Bot
  - Train
---
What if, during a conversation with your chatbot you want the user to opt for a switch to a human agent?

The simplest thing that you can do is adding a specific answer to your Response bot that will switch to a human agent with a specific instruction in the reply.

## Train the ‘talk to agent’ intent

Open your Response bot console. Add a new Question/Answer. Let’s call this intent ‘Talk to agent’. We’ll train this intent with a single phrase (more phrases can be added as a convenience).

![Open your Response bot console](/images/uploads/79357733-b3d5f700-7f40-11ea-89f2-a093329fd273.png "Open your Response bot console")

Now the intent will reply with:

We are putting you in touch with an operator 

\agent

Copy and paste this text in the *Responses* section of the “Talk to agent” intent:

![We are putting you in touch with an operator \agent](/images/uploads/79358037-07e0db80-7f41-11ea-8d3b-ea4064ea2edf.png "We are putting you in touch with an operator \agent")

The **\agent** keyword, at the end of the reply phrase, will never be shown to the enduser. It is an instruction for Tiledesk to switch the conversation to humans. As soon as Tiledesk see this instruction in the text it will remove the current chatbot (your chatbot) from the corresponding conversation and will try to invite a human, following the current department rules. If no agents are available the conversation will wait in the “unserved” queue until an agent becomes available again.

To test the new “Talk to agent” intent we also place a button under every question (using [Microlanguage](https://docstiledesk.netlify.app/chatbot/resolution-bot-images-videos-buttons-and-more)) to allow the user to ask for an agent after each reply. Let’s train, for instance, the *Default Welcome Intent* Intent to show this optional button (using *Microlanguage* you can easily add a button with **\*** symbol (starting a *new line*) followed by **one space** and the **button text**)

Hi! How are you doing? 

\* Just questions 

\* Talk to an agent

![Talk to agent](/images/uploads/image444.png "Talk to agent")

From now on every welcome intent reply the widget will show the “Talk to agent” button.

![Talk to agent button.](/images/uploads/image4441.png "Talk to agent button.")

If we tap the button the “Talk to agent” intent will be invoked and the user will be routed to an agent on the current department (following the department routing rules, opening hours and agents availability).

Do you have any feedback on this article? Please send us your feedback writing an email to [info@tiledesk.com](mailto:info@tiledesk.com)

Enjoy Tiledesk!