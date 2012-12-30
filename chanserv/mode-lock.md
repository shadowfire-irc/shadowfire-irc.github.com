---
layout: page
title: "Mode locks"
description: ""
group: "chanserv"
---
{% include JB/setup %}

### Introduction

ChanServ allows you to define certain channel modes to be always on (or off).
The modes that can be locked are `i`, `k`, `l`, `m`, `n`, `p`,
`s`, and `t`; each of these modes can be locked on, locked off, or not
locked. Use the `+` prefix to lock modes on and `-` to lock modes off.

For more information about channel modes see [Channel modes](../modes/channel.html).


### Syntax

    /msg ChanServ SET <#channel> MLOCK <modes>


### Examples

#### Lock modes on

Set the channel to always be invite-only:

    /msg ChanServ SET #channel MLOCK +i

Set the channel to always be invite-only and private:

    /msg ChanServ SET #channel MLOCK +ip

Set the channel to require the key "pass" to enter:

    /msg ChanServ SET #channel MLOCK +k pass

#### Lock modes off

Set the channel to never be invite-only:

    /msg ChanServ SET #channel MLOCK -i

Set the channel to never be invite-only and private:

    /msg ChanServ SET <#channel> MLOCK -ip

#### Lock mode combinations

Set the channel to never be invite-only and always private:

    /msg ChanServ SET <#channel> MLOCK -i+p


### Removing mode locks

To remove all locked modes, use the following command:

    /msg ChanServ SET <#channel> MLOCK +
