> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/server/messages/timer.md).

# Auto Messages

{% hint style="warning" %}
You can only have **one** auto message per channel, and the interval must be at least **5 minutes**.
{% endhint %}

## Creating an auto message <a href="#creating-an-auto-message" id="creating-an-auto-message"></a>

You can create an auto message with the `timer add` command.

```
Syntax: ;timer add [channel] [interval] [code]
Example: ;timer add #general 10m {embed}$v{description: Hello world}
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_NeS6BXHWd1.png" alt=""><figcaption></figcaption></figure>

## Removing an auto message

You can remove an auto message with the `timer remove` command.

```
Syntax: ;timer remove [channel]
Example: ;timer remove #general
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_w68LfK7159.png" alt=""><figcaption></figcaption></figure>

## Test an auto message

You can test a auto message with the `timer test` command.

```
Syntax: ;timer test [channel]
Example: ;timer test #general
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_hEoPERYygK.png" alt=""><figcaption></figcaption></figure>

## Viewing all system messages

You can use the `timer list` command to view all auto messages.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_Gu5ZcM1SW9.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/server/messages/timer.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
