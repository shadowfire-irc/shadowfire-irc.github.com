---
layout: page
title: "Kill enforce"
description: ""
group: "nickserv"
---
{% include JB/setup %}

This enables kill protection for your nickname.  With kill protection on, if a user tries to take your nick, they will be given one minute to change to another nick, after which they will be forcibly removed from IRC by NickServ.

### Syntax

    /msg NickServ SET KILL {ON | QUICK | IMMED | OFF}

### Options

* `ON` – User is given 60 seconds to change their nickname.
* `QUICK` – User is given 20 seconds to change their nickname instead of the usual 60.
* `IMMED` – User is killed immediately without being warned or given a change to change their nick.

**NOTE:** Improper use of `IMMED` can result in you not being able to use your nick. See [nickserv/Access](access.html) for information on the proper use of `IMMED`.
