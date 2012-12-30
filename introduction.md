---
layout: page
title: "Introduction"
description: ""
group: "general"
---
{% include JB/setup %}

Most, if not all, of Shadowfire's services come with more than adequate help
texts. Reading and understanding the help is strongly encouraged and is more
than likely going to answer your question quicker than if you have to wait
around for someone else to answer.


### Understanding the examples

Lines in examples that start with `>>>` are used to indicate text that is typed
into your IRC client, usually a command that results in a response from the
service.


### Command syntax

Commands specified in these guides use the following formatting rules to
distinguish between different types of parameters:

Mandatory parameters are surrounded with `<>`. e.g. `<foo>`

Optional parameters are surrounded with `[]`. e.g. `[bar]`


### Explore the services

By simply sending the command `HELP` to a service, you will be given the information you need to continue your exploration. Below is an example transcript with ChanServ:

    >>> /msg ChanServ HELP

    -ChanServ(@@services@shadowfire.org@@)- ChanServ allows you to register and control various
    -ChanServ(@@services@shadowfire.org@@)- aspects of channels.  ChanServ can often prevent
    -ChanServ(@@services@shadowfire.org@@)- malicious users from "taking over" channels by limiting
    -ChanServ(@@services@shadowfire.org@@)- who is allowed channel operator privileges.  Type
    -ChanServ(@@services@shadowfire.org@@)- /msg ChanServ HELP COMMANDS for a list of ChanServ commands;
    -ChanServ(@@services@shadowfire.org@@)- to use a command, type /msg ChanServ command, or for more
    -ChanServ(@@services@shadowfire.org@@)- information on a command, type /msg ChanServ HELP command.

(Note that the `HELP` command can also be used with [NickServ](nickserv/about.html) and [AresServ](aresserv/about.html).)

From here you can see that sending the command `HELP COMMANDS` will give you
a list of commands and that `HELP <command_name>` will show you information
specific to that command.

Exploring the services, by finding out what commands are available and what
each command does, can help you learn about useful features that you may not
have known about. Additionally, learning more about services will help you
manage yourself or your users better.


### Ask for help in understanding

People are far more willing to help someone trying to better understand
something than someone who is just looking for a quick fix. People who can help
themselves can help others help themselves and so on.

If you don't understand what the help text for a specific service is saying or what a command does, feel free to [contact](support/contact.html) Shadowfire to ask for help.
