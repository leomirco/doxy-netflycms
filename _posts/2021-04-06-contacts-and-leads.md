---
layout: post
title: Contacts and Leads
date: 2021-04-06T16:42:04.043Z
featured: true
draft: false
comment: false
excerpt: Contacts and Leads
post_image: /images/uploads/service-icon3.png
autore: Andrea
categories: managing_users
tags:
  - functionality
  - Contacts
  - Leads
---
Actually Leads and Contacts are synonyms. We use the term “Lead” in developer docs while we use “Contact” in the UI.

A Contact aggregates requests and metadata collected during conversation(s) with a single user (Anonymous or Authenticated, see next Section).

Example of collected metadata:

* Fullname
* Last name
* Email
* Custom metadata

In general, if the user is connected as “Anonymous” a Lead is created automatically based on the user-id (the user-id is a random generated UUID during the anonymous authentication process). All next user conversations with this UUID will be aggregated in a single Lead.

### An example

When a user first starts a conversation from a browser instance (i.e. Google Chrome) he will be asked for some metadata to follow up a conversation:

![he will be asked for some metadata to follow up a conversation](/images/uploads/pasted-image-0.png "he will be asked for some metadata to follow up a conversation")

Then the user contacts the support another time, as you can see by conversations summary:

![Then the user contacts the support another time, as you can see by conversations summary](/images/uploads/pasted-image-0-1-.png "Then the user contacts the support another time, as you can see by conversations summary")

Now in Contacts module you can search by email ([andrea1@gmail.com](mailto:andrea1@gmail.com)) for the Lead:

![in Contacts module you can search by email](/images/uploads/pasted-image-0-2-.png "in Contacts module you can search by email")

As you can see there is only one Contact with that email. Now in contact detail you can see all the two requests made by this user:

![Contact detail you can see all the two requests made by this user](/images/uploads/pasted-image-0-3-.png "Contact detail you can see all the two requests made by this user")

If the user, with the same email, starts a request from another browser he will be assigned a new Anonymous user-id.

So, for example, if you start a new request from Safari (we started with Chrome browser):

![Starts a request from another browser he will be assigned a new Anonymous user-id.](/images/uploads/pasted-image-0-4-.png "starts a request from another browser he will be assigned a new Anonymous user-id.")

As you can see the user is totally new (a new Anonymous user is created with a new UUID).

Now we insert the same email as in Chrome:

![insert the same email as in Chrome](/images/uploads/pasted-image-0-5-.png "insert the same email as in Chrome")

If we execute the same search as before, by email:

![execute the same search as before, by email](/images/uploads/pasted-image-0-6-.png "execute the same search as before, by email")

Now I find two Contacts, because they have a different UUID as you can see in the detail of the new Contact (Andrea Sp1):

![find two Contacts, because they have a different UUID](/images/uploads/pasted-image-0-7-.png "find two Contacts, because they have a different UUID")

And this new user only made one conversation.

Actually we do not provide a feature to “merge” the two contacts into one (they are effectively the same user, recognized by their identical email, despite the two Contacts have different user-ids). This feature, with the ability to manually create and modify Contacts, is in our roadmap.