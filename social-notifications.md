> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/social-notifications.md).

# Social Notifications

## Supported Platforms <a href="#supported-platforms" id="supported-platforms"></a>

There are nine social notification commands, each with the same subcommands.

* **TikTok** - Dispatched whenever a new video is uploaded.
* **Instagram** - Dispatched whenever a new post or story is uploaded.
* **YouTube** - Dispatched whenever a new video or short is uploaded.
* **Twitter** - Dispatched whenever a new tweet is posted by a user.
* **Twitch** - Dispatched whenever a streamer goes live.

## Commands <a href="#commands" id="commands"></a>

The following examples use the `twitter` command, but the same syntax applies to the other social notification commands.

<details>

<summary>Creating a new feed</summary>

Use the `twitter add` subcommand receive notifications for a specific user.

```
Syntax: ;twitter add [username] [channel] [message]
Example: ;twitter add nike #feed @everyone
```

</details>

<details>

<summary>Removing a social feed</summary>

Use the `twitter remove` subcommand to no longer receive notifications for a specific user.

```
Syntax: ,twitter remove [username]
Example: ,twitter remove nike
```

</details>

<details>

<summary>Viewing all users being monitored</summary>

Use the `twitter list` subcommand to view all users being monitored.

</details>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/social-notifications.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
