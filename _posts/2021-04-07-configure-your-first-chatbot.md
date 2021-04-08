---
layout: post
title: Configure your first chatbot
date: 2021-04-07T16:49:20.254Z
featured: false
draft: false
comment: false
excerpt: Configure your first chatbot
post_image: /images/uploads/service-icon3.png
autore: Andrea
categories: chatbots
tags:
  - functionality
  - Configuration
  - Chatbot
---
Configuring a chatbot in your department can drastically decrease Human Agents workload, simultaneously improving customer satisfaction. Integration of chatbots in your *customer support workflow* provides many benefits:

* **Chatbots are 24/7 available**, for the happiness of end users that always appreciate the “always on” option
* **Chatbots can reply to most common questions**, leaving human agents with more time to manage complex questions

We’ll start our journey in Tiledesk’s chatbots integration creating a simple chatbot that will reply to some common questions and will switch to human agents if needed.

### Create you native Tiledesk bot

Once you create you first project \[link] switch to “Bots” section from the sidebar:

![Create you native Tiledesk bot](/images/uploads/image-1-.png "Create you native Tiledesk bot")

Ignore the predefined identity bot \[link] in the list and press the “ADD BOT” button on the top. A section will open. We will start with Tiledesk “native” bot technology. Tiledesk native bots are question-answer bots, based on a mix of *deep learning* and *fulltext* technologies that provide a “digital assistant” that you can train to provide answers to the most common end users’ questions.

![](/images/uploads/image-1555.png)

First give your new chatbot a name, and provide the necessary description:

![new chatbot a name, and provide the necessary description](/images/uploads/image-2555.png "new chatbot a name, and provide the necessary description")

Now press the CREATE BOT button. As you can see in the next figure your bot is created with some pre-populated list of example question-answer couples.

![press the CREATE BOT button.](/images/uploads/image-3555.png "press the CREATE BOT button.")

You can start to train your chatbot using your FAQs knowledge base, if you have one. Alternatively you can train your bot adding question-answer couples as soon as they are available. Moreover you can also change your chatbot name or profile picture.

Before further training our chatbot, first of all we’ll integrate it in the live-chat workflow to test how it works, how he “greets” our customers and how it can optionally handoff control to human agents.

While our chatbot is already created and fully functional we leave the configuration section and moving to the Routing section (option in the sidebar menu), as in the following picture:

![moving to the Routing section](/images/uploads/image-4555.png "moving to the Routing section")

First we must switch to ON the button on the “Activate Bot” section. Once activated, you can choose our bot Charlie from the “Bot” menu. Leave all other options with their default values, then press UPDATE ROUTING RULES button on the bottom.

To test how Charlie works we can move to the Requests panel (from the sidebar menu) and push the green SIMULATE VISITOR on the top right corner of the window:

![push the green SIMULATE VISITOR on the top right corner of the window](/images/uploads/image-6555.png "push the green SIMULATE VISITOR on the top right corner of the window:")

A new window will open, where you can play with the widget simulating a visitor interaction and test if your configuration is correct. Open the widget pressing the blue button on the bottom right corner:

![Open the widget pressing the blue button on the bottom right corner](/images/uploads/image-7-555.png "Open the widget pressing the blue button on the bottom right corner")

Now press “New conversation”. A new conversation starts, and we will soon receive a welcome message from Charlie: “Hello”.

![press “New conversation”](/images/uploads/image-8555.png "press “New conversation”")

We can change the initial welcome message in a very easy way. Just move back to the Bot section and select Charlie from the list:

![change the initial welcome message](/images/uploads/image-9555.png "change the initial welcome message")

Now from the list choose the **\start** answer, as shown by the arrow in the following picture:

![from the list choose the \start answer](/images/uploads/image-12555.png "from the list choose the \start answer")

The \start answer is the one invoked by Tiledesk as soon as it recognises that a chatbot was activated on the selected department. To change the greeting message that Charlie sends to new users you can modify the \start answer.

Select \start and change the default answer with a new customised greetings message, as in the following picture, then press UPDATE ANSWER button on the bottom:

![press UPDATE ANSWER button](/images/uploads/image-13555.png "press UPDATE ANSWER button")

Now, again, go back to the test widget page, where we will eventually move out of the current conversation and start a new one, just to test the new greeting message:

![new greeting message](/images/uploads/image-14555.png "new greeting message")

Et voilà! Charlie now greets us with our new greeting message.

In the next articles we will learn how to further train our chatbot, how to eventually switch control to a human agent, how to add buttons, send images or videos using the embedded bot micro-language \[link].

Enjoy!

Please feel free to send feedback about this tutorial to [support@tiledesk.com](mailto:support@tiledesk.com). Thanks!