---
layout: page
title: "Passwords"
description: ""
group: "nickserv"
---
{% include JB/setup %}

### Changing Your Password

To change your password, use the following command:

    /msg NickServ set PASSWORD <new-password>


### Retrieving nickname passwords

If you've lost or forgotten your password for your nickname, you can have
NickServ e-mail it to the address the nickname was registered (or updated) with
by using the following command:

    /msg NickServ SENDPASS <nickname>

It is recommended that you keep your NickServ e-mail address up to date, see [nickserv/Email](email.html).
