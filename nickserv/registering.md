---
layout: page
title: "Registering a nickname"
description: ""
group: "nickserv"
---
{% include JB/setup %}

To register your nickname you can use the following command:

    /msg NickServ REGISTER <password> <email>

An email containing an authentication code will be sent to the specified email
address. Once you have received this email you can authenticate your email
address with the following syntax:

    /msg NickServ AUTH <code>

Authentication must be completed within 24 hours or the nickname will removed
from our database. Please note, authenticated nicknames may be removed from our
database if they remain inactive for a period exceeding 90 days.

Once you have successfully registered your nickname and authenticated your
email address, you will be required to identify yourself to NickServ each time
you log on. See [nickserv/Identifying](identifying.html) for more information.
