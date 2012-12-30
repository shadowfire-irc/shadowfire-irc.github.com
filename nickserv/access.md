---
layout: page
title: "Access lists"
description: ""
group: "nickserv"
---
{% include JB/setup %}

Access lists for your nickname are a list of addresses allowed to use nickname, as recognized by NickServ.  If you connect to IRC with an address on this list, you will not be affected by the nick's [nickserv/KillEnforce](kill-enforce.html) setting and, if the [nickserv/Secure](secure.html) option is disabled, you will be able to receive auto-op and other privileges in channels without using the [nickserv/Identifying](identifying.html) command.

Syntax:

    /msg NickServ ACCESS {ADD | DEL | LIST} mask

Examples:

    /msg Nickserv ACCESS ADD nim@caladan.shadowfire.org
    /msg Nickserv ACCESS DEL nim@caladan.shadowfire.org
    /msg Nickserv ACCESS LIST
