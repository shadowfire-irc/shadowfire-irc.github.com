---
layout: page
title: "Security"
description: ""
group: "nickserv"
---
{% include JB/setup %}

Turns NickServ's security features on or off for your nickname.  With `SECURE`
set you must enter your password before you will be recognized as the owner of
the nick, regardless of whether your nick is on the [access list](access.html).
However, if you are on the access list, NickServ will not auto-kill you
regardless of the setting of the `KILL` option.

### Syntax

    /msg NickServ SET SECURE {ON | OFF}
