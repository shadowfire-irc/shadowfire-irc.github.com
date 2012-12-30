---
layout: page
title: "Access levels: Maintenance"
description: ""
group: "chanserv"
---
{% include JB/setup %}

### Introduction

Following on from [Access Levels](access.html); ChanServ has shortcuts to
maintaining your access lists.  These are `VOP`, `HOP`, `AOP` and `SOP`
which represent voice (`+v`), half-op (`+h`), operator (`+o`) and
super-op (`+a` and `+o`) respectively.

**NOTE:** Not all commands will be used in the examples below but they all
behave identically and are thus interchangeable, simply replace the command
name with the one for the mode you are interested in.


### Who can use what?

Using these shortcuts in a channel is restricted to what access level you
currently have in that channel. For example, an `AOP` can modify the `HOP`,
and `VOP` lists, only a channel's founder or a `SOP` can modify the `AOP`
list and only someone with greater than `SOP` (such as the founder) can
modify the `SOP` list.


#### Listing access levels

List all the current users with auto-voice (`+v`):

    /msg ChanServ VOP <#channel> LIST


#### Adding a user

Add a user to the auto-hop (`+h`) access list:

    /msg ChanServ HOP <#channel> ADD <nick>

**NOTE:** The user must have a registered nick to be added to an access list,
see [nickserv/Registering](../nickserv/registering.html) for more information.


#### Removing a user

Remove a user from the auto-hop (`+h`) access list:

    /msg ChanServ HOP <#channel> DEL <nick>
