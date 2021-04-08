---
layout: post
title: "Advanced chatbot styling: buttons"
date: 2021-04-08T09:54:39.472Z
featured: false
draft: false
comment: false
excerpt: "Advanced chatbot styling: buttons"
post_image: /images/uploads/service-icon3.png
autore: Andrea
categories: chatbots
tags:
  - functionality
  - Chatbot
  - Buttons
  - Configuration
---
You can talk to chatbots in two basic ways: NLP (Natural Language Processing) or with static button replies.

With **NLP** processing the chatbot engine tries to process the text typed by the user, extracting and processing the words inside the same text to decode the supposed “user intent”. The intent, in the case of Tiledesk native bot, is the answer for what the user was searching for. NLP is a powerful technology, because provides the user with the freedom to write as he was chatting with a real human (while there is a machine on the other end). But sometimes this freedom is not the best solution.

**Buttons** are an alternative way to help end users to reply to a message. A button, in Tiledesk, simply sends the button-text to the chatbot on the other side of the conversation. So, if the button contains the text “Talk to agent”, after pressing the button this same text will be sent and shown in the conversation as if you typed it manually.

To better understand when and how buttons are a better solution than using NLP, we can start with a practical example.

### NLP example

For this example we can start from our Charlie chatbot in the first tutorial. Just consider, but we’ll return on this later, that the way described in this article to render buttons works on all Tiledesk chatbots, e.g. Native chatbots, External and Dialogflow chatbots.

Now suppose that the user wants to ask something about the type of accounts supported by Quantabank. He can, for example, ask something like this: “what type of accounts do you provide?”. Let’s create the answer to this question.

![Let’s create the answer to this question.](/images/uploads/image-51.png "Let’s create the answer to this question.")

Fill the questions-answer form with the following text:

**Question**

*what types of accounts do you provide?*

**Answer**

*\_\_Quantabank\_\_ actually provides the following account types:*

 *\- Basic Checking Accounts.* 

*\- Savings Accounts.* 

*\- Interest-Bearing Checking Accounts.* 

*\- Money Market Accounts.* 

*\- Brokerage Accounts. What of this accounts are you interested in? (i.e \_Savings account\_)*

Now, to fulfill the user knowledge needs, we should provide to the user additional replies for each of the proposed options. We the purposes of this example can only provide an answer for the “Savings account” question. To accomplish this easy task we must create a new answer. Presse the ***+ New answer*** button in the chatbot Charlie toolbar (as before). Fill the fields with the following data:

**Questions**

*Savings accounts*

**Answer**

*A \_\_Savings account\_\_ is an interest-bearing deposit account held at a Quantabank. Though these accounts you pay a modest interest rate while their safety and reliability make them a great option for parking cash you want available for short-term needs. \[more info](https://quantabank/accounts/savingsaccount)*

Click on CREATE ANSWER. Now we can test all the questions-answers workflow in the SIMULATE VISITOR view (press SIMULATE VISITOR in the Request panel). Click on the widget and press “New conversation”. After the chatbot greetings us with “Hello”, we can type our first question:

![Click on CREATE ANSWER](/images/uploads/image-57.png "Click on CREATE ANSWER")

The chatbot will reply with a list of options in the message body with the final suggestion in the message tail to type the name of one of this options to get more information. We can type “Savings account”, getting the expected result:

![type “Savings account”](/images/uploads/image-58.png "type “Savings account”")

Very good as result, the user got his response and he is probably satisfied with the reply. But he had to type by hand “savings account”. This is an error prone task, because typing often introduce errors and, moreover, typing is tedious for the user. Why writing something when there is a better alternative? Render the accounts as a sort of *options menu*: **the list of available account types**. It’s better in this case to give up on the power of NLP and switch to buttons instead! How to get buttons for the list of accounts?

### Introducing buttons

With Tiledesk it’s very easy to render buttons. Simply place an asterisks (*) on a new line, followed by the text that you want to render in the button. The rendered text will be all the one in the line, trimmed by trailing and leading spaces.

In our case, to render the list of accounts as buttons, we can replace the “-” in the list of the accounts with asterisks (*). It’s also better to refactor the text of our message because the list will be ripped apart from the message and the buttons will be placed after the message text.

So the new answer text will become:

**Question** (don’t change)

*what type of accounts do you provide?*

**Answer** (1. replace – with *, 2. removed tail suggestion to type option’s name):

*\_\_Quantabank\_\_ actually provides the following account types.* 

*Please choose the one you are interested in.* 

*\* Basic Checking Accounts.* 

*\* Savings Accounts.* 

*\* Interest-Bearing Checking Accounts.* 

*\* Money Market Accounts.* 

*\* Brokerage Accounts.*

Every element in the list of the reply message marked with an asterisk (*) will be rendered as a button.

Press UPDATE ANSWER. Now test it in the usual way, moving to Request panel and pressing SIMULATE VISITOR button. Start a new conversation pressing the “New conversation” button (or continue the old one). After the greetings message you can ask your question “what kind of accounts do you provide?”, and this will be the resulting reply:

![SIMULATE VISITOR button](/images/uploads/image-59.png "SIMULATE VISITOR button")

Our list was rendered as a group of buttons, aligned on the right of the widget area. Probably our user will be more happy, having only to click and option on a menù instead of typing an entire text.

What will now happen if we push some of those buttons? Let’s try, i.e. from the last one, “Brokerage Accounts”.

![Let’s try, i.e. from the last one, “Brokerage Accounts”](/images/uploads/image-60.png "Let’s try, i.e. from the last one, “Brokerage Accounts”")

Just wait a couple of seconds and we’ll get the same response as the NLP case:

![Just wait a couple of seconds and we’ll get the same response as the NLP case](/images/uploads/image-61.png "Just wait a couple of seconds and we’ll get the same response as the NLP case")

We’ve seen the power of buttons, and how easy it is to introduce them in our conversations.

Enjoy Tiledesk buttons!

Please feel free to send feedback about this tutorial to [support@tiledesk.com](mailto:support@tiledesk.com). Thanks!