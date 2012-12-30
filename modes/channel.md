---
layout: page
title: "Channel modes"
description: ""
group: "modes"
---
{% include JB/setup %}

Channel modes allow you to specify a precise ruleset which will be implemented in your channel. These modes can be removed or altered by anyone with sufficient channel access, so be careful about who you give that access to!

### Settable by half-ops

#### BAN (+b)

##### Syntax

    /mode <#channel> +b <nick!ident@host>

Bans all users which match the ban mask from the specified channel. Those users
will be unable to rejoin the channel until they are unbanned or made exempt
from channel bans (see mode `+e` below). The mask may contain wildcards such as
`*` and `?`.

##### Examples

Ban all nicknames that begin with *TroubleMaker*:

    /mode #somechannel +b TroubleMaker*!*@*

Bans all users who use "telkomadsl.co.za" as their ISP:

    /mode #somechannel +b *!*@*telkomadsl.co.za


#### BAN EXCEPTION (+e)

##### Syntax

    /mode <#channel> +e <nick!ident@host>

Override a ban for users matching the supplied mask. Those users will be able to join the channel regardless of any bans that may affect them.

##### Examples

Allow anyone called *JohnDoe* to enter the channel regardless of any existing bans:

    /mode #somechannel +e JohnDoe!*@*


### Settable by channel operators

#### NOCOLOUR (+c)

##### Syntax

    /mode <#channel> +c

Blocks all messages which contain mIRC colour codes from being delivered to the
channel. All users in the channel are affected by this channel mode (including
channel operators). A less intrusive method of removing colours from your
channel is to use the `+S` mode detailed below.

#### FLOOD_LIMIT (+f)

##### Syntax

    /mode <#channel> +f <parameters>

This command is used to configure a channel's flood protection to prevent spam
and other undesirable channel behaviour. See [modes/Flood Protection](flood-protection.html) for
further information.

#### JOIN_THROTTLE (+j)

##### Syntax

    /mode <#channel> +j <joins:sec>

Throttles the number of times a user can join the channel in a given number of
seconds. This is helpful if your channel is being spammed by abusive users who
join/part unnecessarily.

##### Examples

Users can only join the channel 3 times every 5 seconds:

    /mode #somechannel +j 3:5

#### LIMIT (+l)

##### Syntax

    /mode <#channel> +l <limit>

Sets a limit on the number of users who can join the channel at any one time.
Users who try and join your channel after this limit is reached will be told
the channel is full and (if used in conjunction with mode `L` (see below)) will
be forwarded to another channel which you can specify.

##### Examples

The channel can only hold 25 users:

    /mode #somechannel +l 25

#### PRIVATE (+p)

##### Syntax

    /mode <#channel> +p

Marks the channel as being private. This mode is widely considered obsolete.
Consider using the SECRET mode (`+s`) below instead.

#### SECRET (+s)

##### Syntax

/mode <#channel> +s

Marks the channel as being secret. Channel will not show up when the `LIST`
command is issued and users will be unable to see the channel in your `WHOIS`
unless they are already members of the channel.

#### SECURED_ONLY (+z)

##### Syntax

    /mode <#channel> +z

The channel will only be accessible by users who are connecting via a secure connection (such as SSL.)

#### NO_CTCP (+C)

##### Syntax

    /mode <#channel> +C

This mode blocks users from sending `CTCP` messages to the channel. This is
useful if you are getting `CTCP SOUND` or `CTCP PING` messages from users.

#### STRIP_BAD_WORDS (+G)

##### Syntax

/mode <#channel> +G

Filters text based on a badword filter.  Words matching the filter will be
replaced with the text: `<censored>`.

#### REGONLY (+M)

##### Syntax

    /mode <#channel> +M

All users who join the channel must have a registered nickname in order to
message the channel. This can be overridden by channel operators by granting an
unregistered user a voice (`+v`).

##### Examples

Only registered nicknames can talk in #shadowfire:

    /mode #shadowfire +M

Allow the unregistered user "Bob" to still talk to the channel:

    /mode #shadowfire +v Bob

#### NOKNOCK (+K)

##### Syntax

/mode <#channel> +K

Setting this mode will block users from using `/KNOCK` to try and access
a channel which is locked by a keyword. This is seldom used.

#### NO_NICK_CHANGE (+N)

##### Syntax

    /mode <#channel> +N

Users will be unable to change their nickname whilst in your channel if this
channel mode is set.

#### NO_KICKS (+Q)

##### Syntax

    /mode <#channel> +Q

Channel operators are blocked from using the `/KICK` command in your channel.
Please note, ChanServ is able to override this mode and therefore you should
restrict access to the ChanServ KICK command if you wish to use `+Q`
effectively. See [chanserv:Access Levels](../chanserv/access.html) for more
information.

#### REGONLY (+R)

##### Syntax

    /mode <#channel> +R

Only registered nicknames are be able to join your channel when this mode is
set.

#### STRIP (+S)

##### Syntax

    /mode <#channel> +S

This channel mode will remove all mIRC colour codes from messages in your
channel. Unlike `NOCOLOUR` (see above), messages which contain colour codes
will still be delivered to your channel, but their colours will be
automatically removed. Channel operators often favour `+S` as it is less
intrusive and will prevent messages from appearing to be "lost" between the
sender and the channel.

#### NO_NOTICE (+T)

##### Syntax

    /mode <#channel> +T

This blocks users from sending `NOTICE`s to the channel.

#### NO_INVITES (+V)

##### Syntax

    /mode <#channel> +V

This mode prevents users from sending channel invites to users outside the
channel.


### Settable by channel owners

#### LINK (+L)

##### Syntax

    /mode <#channel> +L <#channel2>

When the channel is full and the user limit is reached (see LIMIT above), users
will be automatically redirected to `#channel2`. See [modes/Redirecting Users](../modes/redirecting.html) for a more complete overview.

#### AUDITORIUM (+u)

##### Syntax

    /mode <#channel> +u

Sets the channel into auditorium mode. When you join the channel, `/WHO` will
only list the channel operators and you. This makes it appear that only the
channel operators are in the channel. This could be effective in an
online-interview situation or when used in conjunction with a broadcasting bot.


### Settable by services / IRC-ops

#### REGISTERED (+r)

This command can only be issued by a u-lined services server. It marks the
channel as being registered. The default services modes are outlined below.

#### ADMINONLY (+A)

This command can only be issued by an IRC Administrator. Only Server
Administrators and Network Administrators can join the channel.

#### OPERONLY (+O)

This command can only be issued by an IRC Operator. Only IRC-ops can join the
channel.


### Extended ban types

Shadowfire also provides users with the ability to ban users by from other
channels (eg. ban all users from `#lamers`) as well as blocking specific words
from being used by users in your channel. See [modes/Extended Ban Modes](extended-bans.html)
for further information.

### Default Channel Modes

When you join a new (and unregistered) channel, the IRCd will not set any
channel modes other than granting you operator status. When you register
a channel with ChanServ (see [chanserv/Registering](../chanserv/registering.html))
the default channel modes are: `+ntr`

These default modes will be reset every time the channel is empty unless you make use of [chanserv/ModeLock](../chanserv/mode-lock.html).
