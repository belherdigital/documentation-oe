---
title:  API Documentation 
date:   2015-11-26 06:59:46
categories: settings
tags: settings
permalink: /api-documentation/
---
_Note that you need a premium theme to use the API! Orders, Licenses and Coupons are on API v2._

Open eShop have really simple api endpoints that do not require any kind of identification.

## Verify license

    http://YOURDOMAIN.com/api/license/LICENSENUMBER/?domain=DOMAINOFLICENSE

This returns a JSON, TRUE if valid FALSE if not valid or expired.
The parameter domain is optional and in case that is not provided the referrer will be used.

## Download Software

    http://YOURDOMAIN.com/api/download/LICENSENUMBER/?domain=DOMAINOFLICENSE

This will directly download the file assigned to the license.

The parameter domain is optional and in case that is not provided the referrer will be used.

## Get Products

    http://YOURDOMAIN.com/api/products/OPTIONALCATEGORY

Will return a JSON with your products, you can filter with the seoname of a category to get only the products of that category.

You can also sort the results with parameter order1= sort1= and order2= sort2=, allowed fields for order are ‘id_category’,’created’,’updated’,’price’,’title’,’rate’ and you can sort by asc or desc.

### Example

    http://YOURDOMAIN.com/api/products/?order1=price&sort1=desc

This will return the most expensive products firsts.

### Json return example

    [{"id_product":"1","order":0,"title":"Kamaleon","seoname":"kamaleon","skins":"amelia,cerulean,cosmo,cyborg,flatly,journal,readable,simplex,slate,spacelab,united,yeti,bootstrap,cupid,lumen,darkly,shamrock,pinkiepie,superhero,sandstone,paper,oc","url_more":"http:\/\/market.open-eshop.com\/themes\/kamaleon.html","url_buy":"http:\/\/market.open-eshop.com\/themes\/kamaleon.html","url_demo":"http:\/\/market.open-eshop.com\/themes\/demo\/kamaleon.html","url_screenshot":"http:\/\/market.open-eshop.com\/images\/2013\/11\/08\/1\/thumb_kamaleon_1.jpg?v=1438077666","type":"themes","price":"185.00","currency":"USD","price_offer":null,"offer_valid":null,"rate":"5.00","created":"2013-11-08 05:51:14","updated":"2015-07-28 12:01:06","version":"2.0.0","description":"Premium Theme Kamaleon, with 22 skins and more options! \n\nOnly for Open eShop."},{"id_product":"18","order":1,"title":"CZSale","seoname":"czsale","skins":"original,cosmo,cyborg,readable,superhero,paper,sandstone","url_more":"http:\/\/market.open-eshop.com\/themes\/czsale.html","url_buy":"http:\/\/market.open-eshop.com\/themes\/czsale.html","url_demo":"http:\/\/market.open-eshop.com\/themes\/demo\/czsale.html","url_screenshot":"http:\/\/market.open-eshop.com\/images\/2014\/03\/21\/18\/thumb_czsale_1.jpg?v=1438077653","type":"themes","price":"185.00","currency":"USD","price_offer":null,"offer_valid":null,"rate":null,"created":"2014-03-21 05:46:27","updated":"2015-07-28 12:00:53","version":"2.0.0","description":"CZSale is a Bootstrap 3 theme. Everything is fully responsive and it looks great on mobile, tablets, large desktops and all screen sizes.\n\n5 skins included!!\n\nA logo PNG file is also included with the theme."},{"id_product":"19","order":2,"title":"Olson","seoname":"olson","skins":"original,wedding,happy","url_more":"http:\/\/market.open-eshop.com\/themes\/olson.html","url_buy":"http:\/\/market.open-eshop.com\/themes\/olson.html","url_demo":"http:\/\/market.open-eshop.com\/themes\/demo\/olson.html","url_screenshot":"http:\/\/market.open-eshop.com\/images\/2014\/03\/21\/19\/thumb_olson_1.jpg?v=1438077648","type":"themes","price":"185.00","currency":"USD","price_offer":null,"offer_valid":null,"rate":null,"created":"2014-03-21 05:48:47","updated":"2015-07-28 12:00:48","version":"2.0.0","description":"A neatly designed theme with three colors selection options: Original, Wedding and Happy! with thumbnail listings view to suit your digital goods store."}]



## Orders

**Get all orders**

    GET /api/v2/order/?apikey=

You can filter or modify pagination

**Get 1 order**

    GET /api/v2/order/3424/?apikey=

**New order**

Will create a user and mark the order as paid. If user exists will not create it.

    POST /api/v2/order/create?apikey=0V7DlJcojLGu1QgBm9OaLvXZobvPRszq&email=chema@domain.com&id_product=1

Mandatory fields:

+ email
+ id_product
+ apikey

Optional:

+ paymethod = by default will be 'API', recommended to set to the name of the gateway, ex: wallet, paypal, stripe...
+ txn_id = if you have a transaction code from the payment gateway to identify this order
+ pay_date = iff you want to set the payment date to different date than the request. Format in MySQL: 2015-06-28 13:34:34
+ amount = If the amount charged is different than the product price
+ currency = ex: USD, EUR...
+ fee = fee that the payment gateway charged you
+ coupon = Use the COUPON seoname
+ device_id = will set the first license this device_id
+ domain = will set the first license this domain


## Licenses

**Verify license by domain**

    GET http://eshop.lo/api/v2/license/domain/LICENSENuM?domain=somedomain.com

**Verify license by device_id**

    GET http://eshop.lo/api/v2/license/device/LICENSENuM?device_id=device_idnumber

Will return:

    {"valid":true} 

If license is correct not expired etc...

Or

    {"valid":false}


## Get a coupon

    GET /api/v2/coupon/get/COUPONNAME

Returns if found

    {"coupon":{"id_coupon":"6","id_product":null,"name":"6PRCRHMT","notes":null,"discount_amount":"0.000","discount_percentage":"33.000","number_coupons":"1","valid_date":"2023-03-01 00:00:00","created":"2015-08-17 18:12:34","status":"1"}}

Or not found

    {"coupon":false}

You can filter by id product to verify if the coupon works with that product:
    
    GET /api/v2/coupon/get/COUPONNAME?id_product=5

If this returns something different than false then you are safe to make a sale specifying a coupon

    POST /api/v2/order/create?apikey=0V7DlJcojLGu1QgBm9OaLvXZobvPRszq&email=chema@domain.com&id_product=1&coupon=COUPONNAME

This will generate the order with the coupon added already








