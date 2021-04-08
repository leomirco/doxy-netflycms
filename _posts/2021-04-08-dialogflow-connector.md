---
layout: post
title: Dialogflow Connector
date: 2021-04-08T10:45:10.974Z
featured: true
draft: false
comment: false
excerpt: Dialogflow Connector
post_image: /images/uploads/service-icon3.png
autore: Andrea
categories: chatbots
tags:
  - functionality
  - Chatbot
  - Connector
  - Dialogflow connector
---
You can connect your Dialogflow Agents directly to Tiledesk, so they can reply to your customers questions from the Tiledesk widget while you manage complex conversational flows with Google *deep learning* technology integrated in Dialogflow agents. Moreover you can handoff the conversation from your Dialogflow Agent to Tiledesk Human operators whenever is necessary.

To connect your Dialogflow agent you should first of all sign up in Dialogflow, create and train your agent. Once you do these steps ([a guide to start](https://cloud.google.com/dialogflow/docs/quick/build-agent)) you can connect your agent, making it available to your end users. In the next paragraph we’ll see how to create and train a minimalistic Dialogflow agent that will show you how easily you can embed your Agent in Tiledesk.

### Create your Dialogflow agent

For the scope of this tutorial we will create a small Dialogflow Agent. Enter the Dialogflow console and, from the side menù, choose the “Create new agent” option. A form will appear that we should fill as in the following example. We just set the Agent’s name to *bank-help-agent* leaving all the other fields on the default value:

![Create your Dialogflow agent](/images/uploads/image-23.png "Create your Dialogflow agent")

Now press the CREATE button. The agent will be created and we can now see the list of the default Dialogflow intents:

![press the CREATE button.](/images/uploads/image-24.png "press the CREATE button.")

We should modify the training phrases of the Default Welcome Intent, adding a new one. Every time you embed a Bot in Tiledesk it will greet your user as soon as he enters the chat. Tiledesk will trigger the default welcome of your chatbot sending a “\start” message to him. Adding this phrase to the Default Welcome Intent of our agent will ensure that our Agent will greet our user with our favourite welcome message. In the intents list press on “Default Welcome Intent”. Then add the start phrase to your intent, as in the following picture:

![Adding "\start" to the Default Welcome Intent of our agent ](/images/uploads/image-25.png "Adding \"\start\" to the Default Welcome Intent of our agent ")

Now just move on the bottom of our agent just to customize the welcome message. Remove all the other messages and insert only one message, as shown here:

![customize the welcome message](/images/uploads/image-26.png "customize the welcome message")

Press SAVE. Your agent is ready for your integration in Tiledesk. Now let’s embed it in Tiledesk.

### Create your Dialogflow bot in Tiledesk

Now that your Dialogflow agent is available you can create a Tiledesk Dialogflow bot to connect your DF Agent to Tiledesk. Choose “Bots” option, under “Settings”, from the sidebar menu, :

![Choose “Bots” option, under “Settings”, from the sidebar menu](/images/uploads/image-15.png "Choose “Bots” option, under “Settings”, from the sidebar menu")

Press ADD BOT, and select the Dialogflow option:

![Press ADD BOT, and select the Dialogflow option:](/images/uploads/image-17.png "Press ADD BOT, and select the Dialogflow option:")

Now you can see the Dialogflow Agent connection form:

![Now you can see the Dialogflow Agent connection form:](/images/uploads/image-18.png "Now you can see the Dialogflow Agent connection form:")

Fill the form with the needed information. Choose a **name** for your bot, (we chose *Lisa* for this example). Then select a language (i.e. English). Leave empty the Dialogflow knowledge base ID, we will discuss this in a future tutorial. Fill the description field with a description for your bot.

![Choose a name for your bot](/images/uploads/image-20.png "Choose a name for your bot")

Now upload of your Dialogflow credentials file. To reach this goal please follow [this guide](https://developer.tiledesk.com/external-chatbot/build-your-own-dialogflow-connnector/generate-dialgoflow-google-credentials-file) in the Tiledesk developer portal.

Once you have the credentials **.json** file you can drag & drop it in the *Service account private key* field of the form and press CREATE BOT. Now the form will look as in the following picture:

![Once you have the credentials .json file you can drag & drop it in the Service account private key field of the form and press CREATE BOT.](/images/uploads/image-27.png "Once you have the credentials .json file you can drag & drop it in the Service account private key field of the form and press CREATE BOT.")

If you want you can upload the chatbot profile picture. Alternatively the placeholder provided by Tiledesk will be used.

### Test our Dialogflow Agent

Now everything is ready for testing our integration.

Leave the configuration section and move to the Routing section (option in the sidebar menu). Switch the “Activate bot” button to ON, as in the following picture:

![Test our Dialogflow Agent](/images/uploads/image-28.png "Test our Dialogflow Agent")

Now, from the Bot menù, choose Lisa as our bot:

![Now, from the Bot menù, choose Lisa as our bot:](/images/uploads/image-29.png "Now, from the Bot menù, choose Lisa as our bot:")

Leave all the other options with their the default values and press UPDATE ROUTING RULES. Well, our bot is configured and it’s ready to converse with our customers!

To test how Lisa works we can move to the Requests panel (from the sidebar menu) and push the green SIMULATE VISITOR on the top right corner of the window:

![push the green SIMULATE VISITOR on the top right corner of the window](/images/uploads/image-6-6666.png "push the green SIMULATE VISITOR on the top right corner of the window")

A new window will open, where you can play with the widget simulating a visitor interaction with our widget and test if your bot configuration is correct. Open the widget pressing the blue button on the bottom right corner:

![A new window will open, where you can play with the widget simulating](/images/uploads/image-7-6666.png "A new window will open, where you can play with the widget simulating")

Now press “New conversation”. A new conversation starts, and, if our configuration is correct, we will soon receive the welcome message we previously trained Lisa to send us in her *Default Welcome Intent*.

![press “New conversation”. ](/images/uploads/image-30.png "press “New conversation”. ")

\
Well, our chatbot is now embedded and working in Tiledesk. Now we can see how to further train your bot and we’ll discover what we can do combining DIalogflow with Tiledesk.

### Format your chatbot messages

Tiledesk chatbots support markdown formatting. Not all of the markdown formatting is available, but we can do really good formatting with the available commands. To discover all the available formatting options please take a look at [this guide](https://docstiledesk.netlify.app/chatbots/styling-your-chatbot-replies).

Just for example we can write the name of our agent Lisa in bold using the markdown syntax with the double underscore. Try by yourself to introduce some formatting in the Default Welcome Message like in the following example:

![write the name of our agent Lisa in bold using the markdown syntax ](/images/uploads/image-32.png "write the name of our agent Lisa in bold using the markdown syntax ")

Getting this as result on the welcome message:

![Getting this as result on the welcome message:](/images/uploads/image-31.png "Getting this as result on the welcome message:")

Will be rendered like this:

![Will be rendered like this:](/images/uploads/image-34.png "Will be rendered like this:")

But if you want you can use markdown syntax to better render the link, like this:

![But if you want you can use markdown syntax to better render the link, like this:](/images/uploads/image-35.png "But if you want you can use markdown syntax to better render the link, like this:")

That will be rendered as:

![That will be rendered as:](/images/uploads/image-36.png "That will be rendered as:")

To know all that you can do with chatbot syntax please read [this guide](https://docstiledesk.netlify.app/chatbots/resolution-bot-images-videos-buttons-and-more) \[link].

### Handoff to human agents

What if you want your customer, during a conversation with your chatbot, choose to explicitly switch to a human agent to better accomplish the support task and reach his goal?

In this case you should create an intent that replies with a “\agent” text. Tiledesk immediately understands that the actual conversation must switch to a human. Please follow the [Dialogflow Tutorial 4 – Explicit Human handoff with user intent](https://developer.tiledesk.com/apis/tutorials/dialogflow-tutorial-4-explicit-human-handoff) (for opportunity, this article is actually in the developer zone) for a detailed example on how to reach this goal.

Enjoy!

Please feel free to send feedback about this tutorial to [support@tiledesk.com](mailto:support@tiledesk.com). Thanks!