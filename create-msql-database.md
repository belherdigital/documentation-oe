---
title:  How do I create a MySQL database
date:   2014-10-07 06:59:46
categories: get started
tags: get-started
permalink: /create-mysql-database/
---
To start a installation process of Open eShop software you need:

+ the required PHP,
+ MySQL server with a database and a user name.

All of managed web hostings come with some short of automation for this. If yours does not, check our [list of tested hosting providers that work with our software]({{ site.baseurl }}/software-requirements/#where-can-i-host-my-online-store).
To let you know how to do it, we would like to provide you with some videos, done by users, explaining this process in different panels. Feel free to check the available options and choose the best one for you.

+ [CPanel](https://www.youtube.com/embed/YbIn--iNmKE)

To set up a **database using the MySQL Database Wizard:**

1. In the **New Database** field, enter a name for the database.
2. Click **Next Step**.
3. In the **Username field**, enter a name for the user allowed to manage the database.
4. In the **Password field**, type the user’s password (the password must be 7 letters or shorter).
5. For help generating a strong password, click the **Password Generator** button.
6. Retype the password in the **Password** (again) field.
7. Click **Create User**.
8. Select the privileges you wish to grant the user, or select **ALL PRIVILEGES**.
9. Click **Next Step**.
10. cPanel will display a message stating that the database and user account were successfully set up.

+ [Plesk](https://www.youtube.com/embed/ZTEc5epNvI0)
+ [DirectAdmin](https://www.youtube.com/embed/7QGVQau-gCI)
+ [ISPConfig](https://www.youtube.com/embed/6XosdMzU2pQ)


## MySQL (advanced users)

**Step 1:** Login to MySQL ( you will need an account )

    user@server:~$ mysql -u mysql_user -p

_Enter password:_

**Step 2:** Create the Database
    
    mysql > create database db_name;

**Step 3:** Verify that it’s there
    
    mysql > show databases;

**Step 4:** Create the User
    
    mysql > create user db_user;

**Step 5:** Grant privileges while assigning the password
    
    mysql > grant all on db_name.* to 'db_user'@'localhost' identified by 'db_password';

Note: The localhost field usually doesn’t have to be edited, but you can set it to the specific address.

The above example grants all privileges, obviously. But you will likely want to limit privileges under many circumstances. These parameters include select, insert, and delete.

Choose all that apply and separate by comma, thusly:

    mysql > grant select, insert, delete on db_name.* to 'db_user'@'localhost' identified by 'db_password';


_via lanexa.net_






