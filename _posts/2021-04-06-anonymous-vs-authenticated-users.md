---
layout: post
title: Anonymous vs Authenticated users
date: 2021-04-06T17:07:20.881Z
featured: true
draft: false
comment: false
excerpt: Anonymous vs Authenticated users
post_image: /images/uploads/service-icon3.png
autore: Andrea
categories: managing_users
tags:
  - functionality
  - user
  - Anonymous
  - User authentication
---
By default, first time an end-user starts a conversation with Tiledesk (generally from a chat Widget), a new Anonymous user is created. This anonymous user has a unique UUID that is reused in next conversations on the same browser instance. Tiledesk creates a Contact for the anonymous-user if none exists and attaches the new support request to it.

With anonymous users, the Agent has no way to certificate user identity, user email, fullname and other data provided by the user itself.

This will prevent the Agent to provide to this user sensible informations without risk.

Tiledesk provides a secure way, based on JWT, to provide a certified user profile to Agents.

This secure way of providing certified identity is named **authenticated visitor** and is described here:

<https://developer.tiledesk.com/widget/auth>

You can find an example instance of authenticated user in an article (see § *Authentication*) where we describe what an italian University did for his live chat project to provide support and sensible information to his own students:

<https://www.tiledesk.com/tiledesk-for-unisalento>

As you can see, authenticated users differs from anonymous users by the presence of a shield in the user profile image:

![authenticated users differs from anonymous users](/images/uploads/pasted-image-0-8-.png "authenticated users differs from anonymous users")

All the details about authentication are always available to Agents in the *senderAuthInfo* section in the Contact panel and in the Chat side Panel of the current conversation:

![details about authentication are always available to Agents in the senderAuthInfo section](/images/uploads/pasted-image-0-333.png "details about authentication are always available to Agents in the senderAuthInfo section")