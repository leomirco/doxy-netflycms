---
layout: post
title: Whatsapp with Twilio
date: 2021-04-06T14:26:43.344Z
featured: false
draft: false
comment: false
excerpt: Whatsapp with Twilio
post_image: /images/uploads/service-icon3.png
autore: Andrea
categories: integrations
tags:
  - functionality
  - Whatsapp
  - Twilio
  - integration
---
Before you can connect WhatsApp through Twilio with Tiledesk, you will have to purchase a phone number with Twilio and wait for their team to approve your WhatsApp account. **This process takes one week on average**

Once you have your number approved, integrating to Tiledesk should only take 5 minutes.

**Setting Up Twilio:**

A Twilio account (you can start for free)

**Getting a Phone Number:**

After you have created an account with Twilio, you gain access to their Dashboard. All new accounts are created with **$15** of free credit that you can use to buy phone numbers and test the platform

![created an account with Twilio](/images/uploads/image-411.png "created an account with Twilio")

Head over to the [Twilio Dashboard](https://www.twilio.com/console/) and press the red **“Get a Trial Number”** button. Twilio will recommend a phone number based on your location.

![Get a Trial Number  button](/images/uploads/image-511.png "Get a Trial Number  button")

If you don’t have a preference, you can click the **“Choose this Number”** button. However, if you would like to purchase a number from a different country or you would like a different number from the one recommended, you can click on **“Search for a different number.”**

![Choose this Number](/images/uploads/image-611.png "Choose this Number")

**Applying for WhatsApp Access:**

Once you have a Twilio account and an SMS-enabled phone number, you can apply for WhatsApp Access. For this, you will have to click on **“Programmable SMS”** on the Twilio main menu and select **“WhatsApp.”**

![apply for WhatsApp Access](/images/uploads/image-711.png "apply for WhatsApp Access")

A prompt will appear asking you to read and agree to WhatsApp’s terms of service. Once you have done so, navigate to the **“Senders”** tab from the sidebar.

![navigate to the “Senders” tab](/images/uploads/image-811.png "navigate to the “Senders” tab")

Under the WhatsApp Enabled Senders Tab, click **“Sign Up to Receive Updates”**  to start filling out the Twilio WhatsApp Application form.

This will take you to the first form you need to fill. Once you have filled this form, the Twilio team will contact you in a couple of days to let you know that your account is approved. You can move to the next step of the integration then. 

![you have filled this form](/images/uploads/twillio_form_1.png "you have filled this form")

**Creating a WhatsApp API:**

Once approved, go back to Twilio and navigate to **“Programmable SMS”** > **“WhatsApp”** > **“Senders.”** This time you will be able to create Sender, which are WhatsApp Accounts that can send and receive messages.

![WhatsApp Accounts that can send and receive messages](/images/uploads/image-911.png "WhatsApp Accounts that can send and receive messages")

**Profile Information**

Here you have to click on **Plus Sign (+)**  to open the Profile Information Form.

![Profile Information Form](/images/uploads/image-1011.png "Profile Information Form")

This form is where you create your WhatsApp account profile; this information will be visible to anyone that talks to your WhatsApp number. When you have filled out the required fields, click the “Submit Request” button at the bottom of the dialog box.

Once you have received the final approval from Twilio, your account will be ready to be integrated to Tiledesk where you can manage conversations.

![ready to be integrated to Tiledesk where you can manage conversation](/images/uploads/schermata-2020-12-30-alle-10.22.19.png "ready to be integrated to Tiledesk where you can manage conversation")

**Account SID and Auth Token**

Back on the Twilio Dashboard, you should be able to spot the Account SID and Auth Token fields easily.

![Account SID and Auth Token fields easily](/images/uploads/twilio-sid-auth_censored.jpg "Account SID and Auth Token fields easily")

Copy the Account SID and paste it into its respective fields on the Tiledesk Platform. For the Auth Token, you will have to presso the **“Show”** to reveal it first. Then copy and paste it into Tiledesk Platform as well.

**WhatsApp Enabled Number:**

For the API type, select **“WhatsApp”**. This should open up a new field where you can enter your WhatsApp Enabled Number.

Back on the Twilio platform, navigate back to the WhatsApp Enabled Senders page. Under your list of WhatsApp Profiles, click on **“Configure”** next to your approved phone number.

![Configure next to your approved phone number](/images/uploads/schermata-2020-12-30-alle-10.40.31.png "Configure next to your approved phone number")

![](https://i1.wp.com/docs.tiledesk.com/wp-content/uploads/2020/12/Schermata-2020-12-30-alle-10.40.31.png?resize=1016%2C420&ssl=1)

*Sostituire questo screenshot non appena la richiesta viene accettata: <https://www.twilio.com/console/sms/whatsapp/senders>*

In the From field, you will find the WhatsApp Enabled Number. Copy and paste the entire filed into the respective field on Tiledesk.

(Immagine mancante)

**Connecting to the Platform:**

Once you have filled in the fields on the Tiledesk Platform, you will have to paste the Webhook URL into Twilio.

Go back to the configuration menu of your approved WhatsApp number of Twilio. You can do this by clicking **“Configure”** next to your approved phone number under the WhatsApp Senders tab.

Paste the Webhook URL from the Tiledesk Platform into both the “A message Come In” and the “Status Callback URL” fields.

(Immagine Mancante)

Once you have pasted in the Webhook URL into the fields, click **“Configure”**.

Return to the Tiledesk Platform and click “Connect”.

![Return to the Tiledesk Platform and click “Connect”.](/images/uploads/schermata-2020-12-30-alle-10.50.11_censored.jpg "Return to the Tiledesk Platform and click “Connect”.")

Your Space will now be connected to the WhatsApp Official API via Twilio.

(Immagine mancante – WhatsApp mobile)

(Immagine mancante – chat Tiledesk)

All future WhatsApp messages sent to that phone number will appear on te Tiledesk Platform.