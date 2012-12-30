---
layout: page
title: "Identifying"
description: ""
group: "nickserv"
---
{% include JB/setup %}

In order to use a registered nickname, and before you can perform any ChanServ functions, you will be required to identify yourself. You can use the following command:

    /msg NickServ IDENTIFY <password>

Once you have performed the above command, for the **correct** nickname you can check your whois information to confirm you have identified correctly:

    /whois <your_nickname>

If you have indeed identified correctly, the response should include one line that looks like the following:

    -           : is a registered nick
