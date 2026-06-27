> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/server/messages/system.md).

# System Messages

## Commands

There are four system message commands, each with the same subcommands.

* `welcome` - Dispatched whenever a user joins the server.
* `goodbye` - Dispatched whenever a user leaves the server.
* `boost` - Dispatched whenever a user boosts the server.
* `joindm` - Dispatched whenever a user joins the server.

{% hint style="info" %}
The `boost` event is only dispatched if the server has the **Discord System Message** enabled or whenever the user receives the **Server Booster** role which only occurs once.
{% endhint %}

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_hCHUTim30M.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
The following examples use the `welcome` command, but the same syntax is applied for the other system message commands.
{% endhint %}

```
Syntax: ;welcome add [channel] [code]
Example: ;welcome add #general Hi, {user.mention}
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_wvM0SSEqok.png" alt=""><figcaption></figcaption></figure>

## Removing a system message

You can remove a system message with the `welcome remove` command.

```
Syntax: ;welcome remove [channel]
Example: ;welcome remove #general
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_9p6OF1nFRf.png" alt=""><figcaption></figcaption></figure>

## Test a system message

You can test a system message with the `welcome test` command.

```
Syntax: ;welcome test [channel]
Example: ;welcome test #general
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_FNY5TZSr3b.png" alt=""><figcaption></figcaption></figure>

## Viewing all system messages

You can use the `welcome list` command to view all system messages.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_RERmX3YSoQ.png" alt="" width="453"><figcaption></figcaption></figure>

## Ping on Join

Set a normal welcome message but with this embed code:

```
{embed}$v{content: {user.mention}}$v{delete: 1}
```


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/server/messages/system.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
