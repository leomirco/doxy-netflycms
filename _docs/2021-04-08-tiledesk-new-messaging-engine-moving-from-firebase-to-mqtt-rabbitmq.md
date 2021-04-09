---
layout: blog
title: Tiledesk new messaging engine, moving from Firebase to MQTT/RabbitMQ
date: 2021-04-08T19:59:55.237Z
post_image: /images/uploads/image-1888.png
tags: MQTT/RabbitMQ, messaging engine
autore: Andrea
---
Actually Tiledesk uses [Firebase](https://firebase.google.com/) to deliver messages in real time between all the components of the platform (console, web widget, mobile apps etc.) that directly need to exchange messages.

Tiledesk uses the [Chat21](http://www.chat21.org/) chat platform, an open source set of applications, free to use, built and maintained by our Company.Messages are stored both in the Tiledesk database (for analytics, full text search features etc.) and Firebase (just to allow the client apps – ex. iOS App – to get the conversation messages history).

[Here](https://developer.tiledesk.com/architecture/schema) you can find a description of the current Architecture.

![Tiledesk Architecture](/images/uploads/assets_-lz4-zelpfnjxhzk2q1s_-lp7ugv5dbdys9pwrp4d_-lp7uvkrwie1zvyv9bkx_tiledesk-architecture-design.001.jpeg "Tiledesk Architecture")

The blue frame, Chat21 server, is deployed on Firebase cloud, and is built using Firebase Realtime DB + Firebase Cloud functions.Every Client is connected through websockets with Chat21 Server. A mix of events on messages and webhook calls will synchronize Chat21 Server with Tiledesk server. All messages actually are stored on both platforms for different purposes.

![Chat21 Server](/images/uploads/image888.png "Chat21 Server")

### The new engine

The next Tiledesk platform release will have a new, pluggable instant messaging engine, based on [RabbitMQ](https://www.rabbitmq.com/) (server component) and [MQTT](https://en.wikipedia.org/wiki/MQTT) protocol (Firebase will still be still supported).The next version will be released for production in April.

In the **new version**, the blue frame will be a RabbitMQ instance that will only deliver messages, only storing them for the sole mission of delivering.

![The new engine](/images/uploads/image-1888.png "The new engine")

Once delivered, a message is removed from the delivering queue.With the new version messages will only be stored in Tiledesk where it will be easier to manage them applying to each message the policies chosen by the data owner.\
Moreover, with the new Tiledesk version, the messaging engine will be pluggable, so everyone can unplug from our RabbitMQ solution, choosing another engine.