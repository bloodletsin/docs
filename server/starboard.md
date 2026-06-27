> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/server/starboard.md).

# Starboard

## What is Starboard? <a href="#what-is-starboard" id="what-is-starboard"></a>

The starboard is a channel where members can react to messages and after a certain number of reactions, the message will be reposted to the starboard channel.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_ziXlLYxaLU.png" alt=""><figcaption></figcaption></figure>

## Getting started

Before you run any commands, it’s important to use the `starboard enable` command. Otherwise, messages will not be reposted to the starboard channel. You can use `starboard disable` to temporarily stop messages from being reposted.

## Setting the starboard channel

You can use the `starboard channel` command to set which channel messages will be reposted to.

```
Syntax: ;starboard channel [channel]
Example: ;starboard channel #starboard
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_gS0yteytim.png" alt=""><figcaption></figcaption></figure>

## Customizing the starboard <a href="#customizing-the-starboard" id="customizing-the-starboard"></a>

### Changing the reaction threshold

You can change the minimum number of reactions a message needs to be reposted.

```
Syntax: ;starboard count [count]
Example: ;starboard count 3
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_G8eHWI1ROk.png" alt=""><figcaption></figcaption></figure>

### Changing the emoji to watch for

You can set the emoji that members need to react with for a message to be reposted.

```
Syntax: ;starboard emoji [emoji]
Example: ;starboard emoji ⭐
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_j5vD65XQIv.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/server/starboard.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
