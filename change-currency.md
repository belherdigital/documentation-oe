---
title:  How to Change Currency
date:   2014-10-08 06:59:46
categories: settings
tags: settings
permalink: /change-currency/
---
One of the most commonly asked question by our users is how to deal with currency in which prices are displayed. Apparently it caused a lot of problems and misunderstandings. This is why we decided to make some improvements in order to make it less confusing. Here you can find a short tutorial on how to change the currency sign and decimal representation displayed on your site. We use PHP function [money_format](http://php.net/manual/en/function.money-format.php) to solve all problems in a very easy way.

## How to do it

Follow the steps below carefully to set a currency format:<br>
Firstly, you should go to **Settings > General > Money format** and input your preferred price format exactly the way the currency is represented, as in USD for United States Dollars, EUR for Euro, PLN for Polish Zloty and so on. Once you press update then the currency will show next to each amount.

![money format]({{ site.baseurl }}/images/money-format.png)

## Locale and your digital goods store currency

Your locale doesn't only determine your website currency, but also the way of displaying the price (e.g. using point or comma to separate decimals, displaying currency sign before or after the price), differs from country to country. That's why **it is important what locale you're using**.

For example, if you are using **es_ES**, your currency will be recognized as **€**, which is a legal medium of exchange in Spain. Locale is composed by the shortcut of a language and a country - so if you want to have your site in Spanish, but don't want to use Euro as a currency, you need to set your locale, e.g. as **es_MX** - your digital goods currency will be Mexican Peso.

**To rename your locale** go to the /languages/ folder in your installation files and simply change the name of the language file you use eg: /languages/es_ES to /languages/es_MX

If you don't want to use any sign or **use completely different currency** than that one you use in your country, use a locale that doesn't exist, e.g. change /languages/en_US ($) to /languages/en_EN or /languages/es_ES (€) to /languages/es_XX.

Then, in General Settings in the Panel, edit field **Money Format** - if you put there %n only the number will be displayed (e.g. 100 without any sign). If you put $%n price will be displayed in this format: $100, if %n€ system will display 100€ etc.

We hope that our tips are useful for you. when you need support, feel free to post at our forums or send us a support ticket.





