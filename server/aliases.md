> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/server/aliases.md).

# Command Aliases

## Overview

Command aliases allow you to create custom commands that run other commands. This can be useful for creating shorter or more memorable commands for your server. For example, you could create an alias that runs the `role` command with a specific role.

## Creating an alias

You can create an alias using the `alias add` command.

```
Syntax: ;alias add [alias] [command]
Example: ;alias add deport ban
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_URoRLjGmyv.png" alt=""><figcaption></figcaption></figure>

### Predefined arguments <a href="#predefined-arguments" id="predefined-arguments"></a>

You’re able to use predefined arguments in your aliases, however, if you want to use the user’s input as an argument, you have to use `{}`. Keep in mind that the first argument is `{0}`, the second argument is `{1}`, and so on, it doesn’t start at `{1}`.

```
;ban @bender.py Harrassing Members
// {0} would be @bender.py
// {1} would be Harrassing Members
```

Below is an example of an alias that uses predefined arguments:

```
;alias add shh timeout {0} 10m
;shh @bender.py
```

This alias would run the `timeout` command with the first argument being `@bender.py` from the user’s input and the second argument being `10m` as predefined.

## Removing an alias

You can remove an alias using the `alias remove` command.

```
Syntax: ;alias remove [alias]
Example: ;alias remove deport
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_vMHEk7HIvC.png" alt=""><figcaption></figcaption></figure>

## Viewing all aliases

You can use the `alias list` command to view all aliases.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_4OzzQjAXuK.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/server/aliases.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
