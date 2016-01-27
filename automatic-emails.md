---
title:  Automatic emails sent to users
date:   2015-01-06 06:59:46
categories: content
tags: content
permalink: /automatic-emails/
---
When user of your website does certain actions, e.g. register, purchase a produce or request to change the password, he receives an **automatic email for confirmation**. To see and manage those emails go to **Panel** and choose **Content > Email** from the left sidebar. 

Email templates are already created and translated to multiple languages. You can **Edit** them according to your needs by clicking blue button next to the template.

![automatic emails]({{ site.baseurl }}/images/automatic-emails.png)

Be sure to set **locale** that you are currently using for your site (see: [How to translate and change language?]({{ site.baseurl }}/change-language)). You can edit **title** of the email, its **body** and the **senders email** displayed. For everything to work properly you need to remember to choose the **type: email** and click on **status** check box to make it **active**.

## Available templates of emails

**Change Password (auth-remember):**<br>
Sent to user for confirmation after request to change password 

**Welcome to [SITE.NAME]! (auth-register):**<br>
Welcoming email sent to user after completing registration, reminding data for logging it 

**[EMAIL.SENDER] wants to contact you! (contact-admin):**<br>
Message sent to admin when a visitor uses a contact form 

**New reply: [TITLE]  (new-reply):**<br>
Email sent to user or admin when there is a new reply on the ticket

**Purchase Receipt for [PRODUCT.TITLE]  (new-sale):**<br>
Message sent to inform user about the purchase

**Product updated [TITLE]:  (product-update)**<br>
Email sent to inform users when a product is updated 

**Ticket assigned to you: [TITLE]  (assign-agent)**<br>
Message to inform admin or moderator that a ticket is assigned to them 

**New review for [TITLE]  [RATE]: (review-product)**<br>
Message sent to inform admin about a new review of a product

**New support ticket created [TITLE]  (new-ticket)**<br>
When a new ticket is created by a user, this email is sent to admin 

**Congratulations! New affiliate commission [AMOUNT]  (affiliate-commission)**<br>
Message is sent to user about an affiliate sale on the website

**Password Changed [SITE.NAME]  (password-changed)**<br>
Message to inform user that his password has been changed

**Receipt for [ORDER.DESC] #[ORDER.ID] 	(new-order)**<br>
Message sent to inform user about an order and to complete the payment (Checkout URL) 




























