---
title:  How to translate and change language?
date:   2014-05-08 06:59:46
categories: content
tags: content
permalink: /change-language/
---
When your online store is becoming more international, changing languages and editing translations will be necessary. Our OE script offers current translations in two languages:

+ English (US)
+ Spanish

The feature of setting up a new language just with a one click seems to be very easy, isn't it? So make these simple steps following our hints:

## How to change language?

1. Go to your **Admin Panel**
2. Choose **Content > Translations** from the left sidebar
3. From the **list of available language versions** choose your locale
4. Press **Activate** button next to the locale you've chosen
5. The language of your eCommerce Website is already changed!

![translations]({{ site.baseurl }}/images/translations.png)

When your website is already translated, you may wish to change texts and some phrases. Modifying this function is also very simple thing. You can **edit translation** by clicking yellow button with a pen.

## How to translate

+ Open your Open eShop folder/translations/
+ Create a copy of one of the existing translation files
+ Rename the new file to the language you want to translate to e.g. nl_NL
+ Go to your **Admin Panel > Content > Translations**
+ Pick the language that you created (as shown in the picture below) and press on **Edit**

![translations2]({{ site.baseurl }}/images/translations2.png)

+ Fill the translation boxes with the new text

![translations3]({{ site.baseurl }}/images/translations3.png)

+ Save
+ Send us the file after everything is done (would help us a lot)

**Troubleshooting:**

+ Be sure your hosting has the locales (you can check in unix with command locale -a) if not the site will not use the language you choose.
+ You need the .mo file, this is the one that really matters to the system.
+ You might need to change the HTML charset or the collation for your DB depending on your locale.
+ Check the permissions for the files .po .mo the should have 755.
+ For more help please ask in the forum.

**Help us improve!**

If you would like to **translate Open eShop to another language**, please feel free to [contact us](https://open-eshop.com/contact/) and we would definitely like it if you send us any updated/new version of a translation.



