---
layout: post
title: Styling your chatbot replies
date: 2021-04-08T08:33:31.122Z
featured: false
draft: false
comment: false
excerpt: Styling your chatbot replies
post_image: /images/uploads/service-icon3.png
autore: Andrea
categories: chatbots
tags:
  - functionality
  - chatbot
  - ResolutionBot
---
Tiledesk provides an easy way to style your chatbot reply messages using [Markdown](https://www.markdownguide.org/basic-syntax/) syntax. We can start play with markdown with a Tiledesk native bot, but this syntax si supported also by every external bot as well as Dialogflow native bot integration.

**\*NOTE**: Markdown syntax is only supported by the native Tiledesk widget (native channel). If your chatbot must work on different/multiple channels (e.g. Facebook) you can’t use Markdown because it is not directly supported. If you use Markdown syntax to show some media (e.g. images) you can use the alternative microlanguage syntax where supported (i.e. [Dialogflow connector](https://docs.tiledesk.com/knowledge-base/microlanguage-for-dialogflow-images-videos/)).*

We can start from our previous created **Charlie** chatbot in the [last tutorial](https://docstiledesk.netlify.app/chatbots/configure-your-first-chatbot), enhancing the power of his replies using Markdown language formatting.

### Hyper-textual links

Supposing that our chatbot works as a banking supporter, we can add a new question-answer couple that replies to the common question “How can I open a new account?”. Move to the bot section, select Charlie from the bots list, then, using the toolbar, press “+ New answer” botton:

![press “+ New answer” botton](/images/uploads/image-37.png "press “+ New answer” botton")

Now we can write the question in the first field, followed by the answer in the following one. Then press the SAVE button.

![press the SAVE button](/images/uploads/image-39.png "press the SAVE button")

Press SIMULATE USER in Request panel (see [previous tutorial](https://docs.tiledesk.com/knowledge-base/styling-your-chatbot-replies/)) and let’s try this new chatbot answer training:

![SIMULATE USER](/images/uploads/image-40.png "SIMULATE USER")

Well, as we can see, *urls* pasted into a message are automatically rendered as hyper-textual links. For most cases this is enough. But sometimes we need to alias a rendered link with a custom text. Markdown syntax comes in help this time.

We can render a link with an alternative text enclosing the desired rendered text in brackets (e.g., `[this guide]`) and then follow it immediately with the URL in parentheses (e.g., `(https://quanta.bank/newbankaccount)`).

Modify our Charlie reply to use this new syntax:

![press UPDATE ANSWER](/images/uploads/image-42.png "press UPDATE ANSWER")

Now press UPDATE ANSWER, then, in the simulator, start a new conversation asking the same question, to trigger the same chatbot reply. This is our new message.

![The reply looks as expected](/images/uploads/image-41.png "The reply looks as expected")

The reply looks as expected, with our text rendered, instead of the original URL.

### Images

To add an image, place an exclamation mark (`!`), followed by *alt text* in brackets, and the path or URL to the image asset in parentheses. To test image embedding we can add a new answer, something like the following:

![To add an image, place an exclamation mark (!)](/images/uploads/image-49.png "To add an image, place an exclamation mark (!)")

You should write the image link in this way:

*!\[global](https://i.pinimg.com/236x/9f/df/c4/9fdfc456ce9b829697dac8d44052ba04.jpg)*

The message will be rendered like in the following picture:

![The message will be rendered like in the following picture](/images/uploads/image-48.png "The message will be rendered like in the following picture")

### Other formatting options

#### Bold

What if you want to emphasise some parts of your message with some bold text? With embedded markdown this is a very easy task. To bold text, add two asterisks or underscores before and after a word or phrase. To bold the middle of a word for emphasis, add two asterisks without spaces around the letters (look [here](https://www.markdownguide.org/basic-syntax/#bold) for more details).

![To bold text, add two asterisks or underscores before and after a word or phrase](/images/uploads/image-45.png "To bold text, add two asterisks or underscores before and after a word or phrase")

Now “right documents” will be rendered in bold:

![Right documents will be rendered in bold](/images/uploads/image-43.png "Right documents will be rendered in bold")

#### *Italic*

To italicize text, add one asterisk or underscore before and after a word or phrase. To italicize the middle of a word for emphasis, add one asterisk without spaces around the letters.

![To italicize text, add one asterisk or underscore before and after a word or phrase](/images/uploads/image-46.png "To italicize text, add one asterisk or underscore before and after a word or phrase")

just placed a single _ around the phrase: \_right documents\_”

![just placed a single _ around the phrase: _right documents_”](/images/uploads/image-47.png "just placed a single _ around the phrase: _right documents_”")

*right documents* is now in italic!

Enjoy!

Please feel free to send feedback about this tutorial to [support@tiledesk.com](mailto:support@tiledesk.com). Thanks!