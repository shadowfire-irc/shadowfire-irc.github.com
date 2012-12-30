---
layout: page
title: "Operator-less channels"
description: ""
group: "chanserv"
---
{% include JB/setup %}

### Running without operators

As we all know one of IRC's special features is the users who go on wild power
trips. Their aim is to gain op status in every channel for the sole purpose of
wielding it against other people at every opportunity.

This unfortunate consequence is a result of the permissions system of IRC which
should actually have been done away with when Services were introduced.

Fortunately, you can rectify this for your channel by doing the following:

    /msg ChanServ LEVELS <#channel> DISABLE AUTOPROTECT
    /msg ChanServ LEVELS <#channel> DISABLE AUTOOP
    /msg ChanServ LEVELS <#channel> DISABLE AUTOHALFOP
    /msg ChanServ LEVELS <#channel> DISABLE AUTOVOICE
    /msg ChanServ LEVELS <#channel> DISABLE HALFOP
    /msg ChanServ LEVELS <#channel> DISABLE PROTECT

While this might frighten people into thinking their channel is highly at risk
without active ops to keep bots and so on in check, this is actually the most
effective way to run a channel.

Without operators having automatic explicit access to `/kick`, they are less
likely to abuse it - people are more at ease, and the point of channel wars and
op wars is inherently removed at the source of the problem. This also means
that the automated protections we have built into the server are far more
effective. They will moderate a channel automatically when it is flooded, or
the channel administrators can invoke ChanServ `KICK` and `OP` commands only
when needed.

### Running in secret

Most people consider it hard to run a channel in private modes. This is because
the private modes are generally quite badly thought out. Invite-only mode is
actually the best way to run a channel in secret.

A relatively unknown mode makes it possible to run a channel in invite-only
mode: `+I`, or invite exception list. So long as the channel is actively
populated you can add user masks to the invite exception list. For example, we
can add the nickname `joesoap` to the invite exception list so that he may join
without an invitation:

    /mode #my_channel +I joesoap!*@*

The ChanServ `INVITE` command can be used to request ChanServ to invite you to the channel.

**NOTE:** [nickserv/AutoJoin](../nickserv/auto-join.html) will automatically
invite you where possible, allowing you to bypass invite-only mode when
connecting to the network.
