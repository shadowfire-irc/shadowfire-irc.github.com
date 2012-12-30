---
layout: page
title: "Access levels"
description: ""
group: "chanserv"
---
{% include JB/setup %}

### Introduction

Access levels provide the ability to specify different degrees of channel
privileges (voice, protection, etc.) for users, specified by the *access
level*. Unless otherwise specified, assume default access levels in examples.


### Understanding access levels

Access levels can be confusing at first, this section will try to clarify what
they are and how to use them. The default ChanServ access levels are listed at
[Default Access Levels](access-default.html).

Retrieve a list of the current access levels:

    /msg ChanServ LEVELS <#channel> LIST

Give a user named `JoeSoap` voice (`+v`) in the channel `#testchannel` so he may talk even when the channel is moderated:

    /msg ChanServ ACCESS #testchannel ADD JoeSoap 30

If, for example, you have 100 users in your channel (with the default access
levels) with access level 30 (i.e. get auto-voiced by ChanServ on joining of
the channel) and you want to promote them to channel operators, there are two
options:

 1. Change all users' access levels to 50 (assuming default access levels)
 2. Change the auto-op level to 30

Set the auto-op level to 30 as follows:

    /msg ChanServ LEVELS <#channel> SET <type> <level>

Specific to our example:

    /msg ChanServ LEVELS <#channel> SET AUTOOP 30
    /msg ChanServ LEVELS <#channel> DISABLE AUTOVOICE


### Trouble free access levels

There are some shortcut commands for managing the most common operations in an
easier fashion. More information about these can be found by reading
[Maintaining access levels](access-maintenance.html).


### Examples

#### Listing access levels

List the current database of users and their respective access level:

    /msg ChanServ ACCESS <#channel> list

#### Adding a user to the access list

Add a new user to the access list with an access level:

    /msg ChanServ ACCESS <#channel> ADD <nickname> <access level>

#### Modifying a user's access level

To change a user's previously set access level, use the same command as for
adding a new user with the new access level.

#### Deleting a user from the access list

Delete a user from the access list:

    /msg ChanServ ACCESS <#channel> DEL <nickname>
