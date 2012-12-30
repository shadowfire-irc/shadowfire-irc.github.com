---
layout: page
title: "Extended ban modes"
description: ""
group: "modes"
---
{% include JB/setup %}

Extended ban modes are special parameters that can be passed to the ban (`+b`) channel mode.

### Quiet

#### Syntax

    ~q:<mask>

People matching this ban may still join but will be unable to speak.

#### Examples

    /mode <#channel> +b ~q:*!*@blah.com


### Nick change

#### Syntax

    ~n:<mask>

People matching this ban cannot change their nickname unless they have `+v` or higher.

#### Examples

    /mode <#channel> +b ~n:*!*@*.aol.com


### Channel ban

#### Syntax

    ~c:[prefix]<channel>

If the user is in the specified channel then they will be unable to join.
Optionally a prefix can also be specified (`+ % @ & ~`) to match users who have
that mode (or higher) on the specified channel.

#### Examples

    /mode <#channel> +b ~c:#lamers
    /mode <#channel> +e ~c:@#trusted


### Real name

#### Syntax

    ~r:<realname>

If the realname of a user matches this then they are unable to join.

**NOTE**: an underscore (`_`) matches both a space (` `) and an underscore (`_`).

#### Examples

    /mode <#channel> +b ~r:*Stupid_bot_script*


### Text ban

#### Syntax

    ~T:block:<text>

Bans `text` from being mentioned in the channel by anyone with a lower status
than half-op (`%`). Colour and control codes are stripped from the text before
the comparison.

#### Examples

    /mode <#channel> +b ~T:block:*is_using*

**NOTE**: These ban types are also supported in the channel exception list `+e`. See [Channel modes](channel.html) for more information.
