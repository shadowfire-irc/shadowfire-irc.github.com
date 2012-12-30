---
layout: page
title: "Registering a channel"
description: ""
group: "chanserv"
---
{% include JB/setup %}

In order to register a channel the following conditions need to be met first:

 * The channel needs to be unregistered;
 * Your nickname needs to be registered (see [nickserv/Registering](../nickserv/registering.html));
 * You need to be a channel operator in that channel.

Once these conditions are met you can use the following command to register a channel:

    /msg ChanServ REGISTER <#channel> <founder_password> <brief_channel_description>


### Example

    /msg ChanServ REGISTER #Shadowfire founderpassword This is the Shadowfire help channel.

To drop (unregister) a channel see [chanserv/Unregistering](unregistering.html).
