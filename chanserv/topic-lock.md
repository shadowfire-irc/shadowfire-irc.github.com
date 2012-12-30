---
layout: page
title: "Topic lock"
description: ""
group: "chanserv"
---
{% include JB/setup %}

### Introduction

Topic locking is a ChanServ command which allows you to lock (fix) the topic,
meaning that ChanServ will retain a particular topic regardless of any attempts
to modify the topic with the `/topic` command.

Use the ChanServ `TOPIC` command to change the topic, regardless of whether it is locked.


### Syntax

    /msg ChanServ SET <#channel> TOPICLOCK [ON | OFF]

    /msg ChanServ TOPIC <#channel> <topic>


### Examples

Set the topic of #channel to "Hello world":

    /msg ChanServ TOPIC #channel Hello World
