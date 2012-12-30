---
layout: page
title: "Passwords"
description: ""
group: "chanserv"
---
{% include JB/setup %}

### Retrieving channel passwords

If you have lost or forgotten the password for a registered channel you can request that ChanServ email it to you if you meet the following conditions:

 * You are the founder of that channel;
 * You have identified for your nickname (see [nickserv/Identifying](../nickserv/identifying.html)).

Then you can use the following command to retrieve the password:

    /msg ChanServ SENDPASS <#channel>
