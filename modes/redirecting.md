---
layout: page
title: "Redirecting users"
description: ""
group: "modes"
---
{% include JB/setup %}

In some cases, you may want / need to move to a new channel and would like all users who were previously joining a channel to now join a new one. This can be achieved by combining the limit mode (`+l`) with the link mode (`+L`). See [Channel modes](channel.html) for more information on these modes.

By setting the limit of a channel to 1 (the lowest possible value) and the channel link value to the new channel's name, you can redirect all new users will join the new channel. As the lowest possible value of `+l` is 1, you will need at least one user to reside in the old channel. An example of redirecting users of `#sadpeople` to `#happypeople` is as follows:

    /mode #sadpeople +l 1
    /mode #sadpeople +L #happypeople
