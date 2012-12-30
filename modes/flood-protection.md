---
layout: page
title: "Flood protection"
description: ""
group: "modes"
---
{% include JB/setup %}

The `+f` channel mode provides comprehensive flood protection for a channel,
this mode allows you to prevent join, nick change, CTCP, text and knock floods.

**NOTE**: The command below does not follow all of the rules set out in the
[introduction](../introduction.html). In this case `[]` are literal square
brackets while `{}` are the optional parameters. This is how the `+f` mode
works.

### Syntax

    /mode <#channel> +f [<amount><type>{#<action>}{,...}]:<seconds>

### Parameters

#### Amount

This specifies the number of times the desired flood type (see below) must
occur before the action is taken.

#### Type

Type | Name        | Default action | Other available actions |
:----|:------------|:---------------|:------------------------|
c    | CTCP        | +C             | m, M                    |
j    | Join        | +i             | R                       |
k    | Knock       | +K             |                         |
m    | Messages    | +m             | M                       |
n    | Nick change | +N             |                         |
t    | Text        | kick           | b                       |
{:class="table table-striped"}

The difference between the `m` and `t` types is that `m` is tallied for any and
all user text in the channel and `t` is tallied per user.

#### Action

This is the action to take / mode to set when the flood protection is
triggered. See the above table for more information.

Actions may also specify a time (in minutes) after which the specific action
will be reversed. See the examples below for more information.

#### Seconds

This is the time period (in seconds) in which the number of events, specified
by the `amount` parameter, must occur.

### Examples

After __20 joins__ in __15 seconds__, __set `+R`__ and __unset it it after 5 minutes__:

    /mode <#channel> +f [20j#R5]:15

After __10 joins__ in __15 seconds__, __set `+i`__ and __unset it after 13 minutes__. Also, if __5 lines from the same user__ in __15 seconds__ occur, kick them:

    /mode <#channel> +f [10j#i13,5t]:15
