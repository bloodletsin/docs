> For the complete documentation index, see [llms.txt](https://docs.bleh.rest/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.rest/server/starboard.md).

# Starboard

## What is Starboard? <a href="#what-is-starboard" id="what-is-starboard"></a>

The starboard is a channel where members can react to messages and after a certain number of reactions, the message will be reposted to the starboard channel.



## Getting started

Before you run any commands, it’s important to use the `starboard enable` command. Otherwise, messages will not be reposted to the starboard channel. You can use `starboard disable` to temporarily stop messages from being reposted.

## Setting the starboard channel

You can use the `starboard channel` command to set which channel messages will be reposted to.

```
Syntax: ;starboard channel [channel]
Example: ;starboard channel #starboard
```



## Customizing the starboard <a href="#customizing-the-starboard" id="customizing-the-starboard"></a>

### Changing the reaction threshold

You can change the minimum number of reactions a message needs to be reposted.

```
Syntax: ;starboard count [count]
Example: ;starboard count 3
```



### Changing the emoji to watch for

You can set the emoji that members need to react with for a message to be reposted.

```
Syntax: ;starboard emoji [emoji]
Example: ;starboard emoji ⭐
```
