---
layout: page
title: "Automatically joining channels"
description: ""
group: "nickserv"
---
{% include JB/setup %}

NickServ can help you automatically join the channels you use regularly. If a particular channel in your autojoin list is invite only, and you have sufficient access for the channel, NickServ will invite you before joining you to the channel.

### Managing autojoin channels

**NOTE:** Before any of these commands are available, you first need to identify yourself to NickServ. See [nickserv/Identifying](identifying.html) for more information.

Adding a channel to the autojoin list can be done with the following command:

    /msg NickServ AJOIN ADD <channel>

Removing a channel is done with:

    /msg NickServ AJOIN DEL <channel>

You can also list the channels you are currently automatically joining with:

    /msg NickServ AJOIN LIST
