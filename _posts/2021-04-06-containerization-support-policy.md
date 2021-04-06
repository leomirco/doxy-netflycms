---
layout: post
title: Containerization Support Policy
date: 2021-04-06T17:24:03.332Z
featured: false
draft: false
comment: false
excerpt: Containerization Support Policy
post_image: /images/uploads/service-icon3.png
autore: Ilenia
categories: self_hosted
tags:
  - functionality
  - support
  - HelpDesk
---
Tiledesk supports deployment using the open industry-standard technology Docker for containerization and Kubernetes for orchestration. We provide reference Docker images and a reference orchestrated deployment using Kubernetes and Helm. These deployment templates are there to enable customers to understand the best practices for deployment of our platform.

As with traditional on premise deployment methods, customers may wish to customize or build upon the technology and ideas within our deployment templates. The deployment templates provide a starting point for customers to simplify the creation of deployments unique to their own needs and skill sets.

Where customers make this kind of customization, Tiledesk will support the underlying images, providing they are using the supported infrastructure components listed on our product supported stack configurations.

![supported infrastructure components listed](/images/uploads/deployment-support.png "supported infrastructure components listed")

The above illustration shows four deployment options, Tiledesk creates and supports only the software represented as App1, App2, and App3. Tiledesk doesn’t create or support anything else in the diagram – that’s all considered to be “infrastructure”.

There are different ways to deploy Tiledesk software into an infrastructure before it can run. A few options include using custom shell scripts, installers, Docker Compose, Kubernetes, Docker Enterprise, OpenShift, Heroku, Google Cloud, AWS ECS, AWS EKS and so on.

Tiledesk doesn’t create or support any deployment tool and customers may choose the deployment tool they feel most comfortable with, often this will be based on a company standard. Customers must have the skills and knowledge needed to use their chosen deployment tool effectively. Tiledesk cannot provide assistance on the deployment tool/mechanism, our approach is to support industry-leading standards and best practices to give customers the choice of platforms on which to deploy.

Tiledesk aims to update the reference Docker images as the underlying operating system and libraries are released, however, as we’re building upon the work of others, we cannot give guarantees and assurances on the timeliness of upgrades and patches for security issues as we would for our own software.