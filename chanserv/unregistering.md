---
layout: page
title: "Unregistering a channel"
description: ""
group: "chanserv"
---
{% include JB/setup %}

Just like you can register a channel you too can unregister one, referred to as
"dropping" a channel, by using the ChanServ `DROP` command. In order to drop
a channel you will need to identify yourself to ChanServ using the `IDENTIFY`
command:

    >>> /msg ChanServ IDENTIFY #some_channel the_chanserv_password
    -ChanServ(services@shadowfire.org)- Password accepted -- you now have founder-level access to #some_channel.

Once you've successfully identified yourself to ChanServ for your channel you
can proceed to drop it:

    >>> /msg ChanServ DROP #some_channel
    -ChanServ(services@shadowfire.org)- Channel #some_channel has been dropped.

You can check that the channel was dropped by doing:

    >>> /msg ChanServ INFO #some_channel
    -ChanServ(services@shadowfire.org)- Channel #some_channel isn't registered.
