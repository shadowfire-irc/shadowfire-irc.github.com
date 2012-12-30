---
layout: page
title: "Linking nicknames"
description: ""
group: "nickserv"
---
{% include JB/setup %}

Unregistered nicknames can be linked to previously registered nicknames without needing to register them. Linked nicknames inherit the access levels and other network services permissions from the original nickname. Nicknames may only have a limited number of nicknames linked to them. The follow command can be used to link a nickname:

    /msg NickServ LINK <nickname>

To unlink a nickname use the following command:

    /msg NickServ UNLINK <nickname>

To view the list of currently linked nicknames use the following syntax:

    /msg NickServ LISTLINKS
