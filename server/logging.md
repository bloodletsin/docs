> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/server/logging.md).

# Logging

## Overview

Logging allows you to log events in your server. This can be useful for keeping track of what’s happening in your server.

## Adding a logging event <a href="#adding-a-logging-event" id="adding-a-logging-event"></a>

You can add a logging event using the `logs add` command.

{% hint style="info" %}
Available logging events are `messages`, `members`, `roles`, `channels`, `moderation`, `appeals`, `guild` and `voice`.
{% endhint %}

```
Syntax: ;logs add [event] [channel]
Example: ;logs add messages #server
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_Dj1FfyGZcP.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_0DKaoZGT9m.png" alt=""><figcaption></figcaption></figure>

## Removing a logging event

You can remove a logging event using the `logs remove` command.

```
Syntax: ;logs remove [event]
Example: ;logs remove messages 
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_K4lx1c0W48.png" alt=""><figcaption></figcaption></figure>

## Ignoring a member or channel <a href="#ignoring-a-member-or-channel" id="ignoring-a-member-or-channel"></a>

You can ignore and unignore a member or channel from being logged using the `log ignore add` command.

```
Syntax: ;level ignore add [target]
Example: ;level ignore add #general

Syntax: ;level ignore remove [target]
Example: ;level ignore remove #general
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_YWWx5LAKFu.png" alt=""><figcaption></figcaption></figure>

## View all enabled logging events

You can use the `logs list` command to view all enabled logging events.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_O9J8PoRkeG.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/server/logging.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
