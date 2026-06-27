> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/server/messages/responder.md).

# Auto Responders

## Creating an auto responder <a href="#creating-an-auto-responder" id="creating-an-auto-responder"></a>

You can create an auto responder with the `autoresponder add` command.

{% hint style="warning" %}
The **trigger** and **response** must be separated by a comma (`,`).
{% endhint %}

{% hint style="info" %}
The `message` parameter can be raw text or an [embed](https://github.com/EvelinaServices/docs/blob/main/server/messages/broken-reference/README.md) with dynamic [variables](/resources/scripting/variables.md).
{% endhint %}

```
Syntax: ;autoresponder add [response]
Example: ;autoresponder add hello, hello world --not_strict --delete --reply
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_95BAukreZ2.png" alt=""><figcaption></figcaption></figure>

### Available flags

<details>

<summary>Not strict</summary>

The `--not_strict` flag will search for the trigger anywhere in the message. For example, if the trigger is `hello`, it will respond to `hello there`.

</details>

<details>

<summary>Delete trigger</summary>

The `--delete` flag will delete the trigger message after the response is sent.

</details>

<details>

<summary>Reply to trigger</summary>

The `--reply` flag will reply to the trigger message.

</details>

## Removing an auto responder

You can remove an auto responder with the `autoresponder remove` command.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_9DJZQW7p8N.png" alt=""><figcaption></figcaption></figure>

## Viewing all auto responders

You can use the `autoresponder list` command to view all auto responders.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_0eBkheb9tL.png" alt="" width="236"><figcaption></figcaption></figure>

## Removing all auto responders

You can use the `autoresponder clear` command to remove all auto responders.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_66PwpxbpWE.png" alt="" width="438"><figcaption></figcaption></figure>

## Restricting auto responders

You can restrict an auto responder to a specific user, channel or role with the `autoresponder allow` command.

```
Syntax: ,autoresponder allow [trigger] [target]
Example: ,autoresponder allow hello bender.py
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-01-19%20190830.png" alt=""><figcaption></figcaption></figure>

## Disabling auto responders

You can disable an auto responder in a specific channel or for a specific role/user with the `autoresponder deny` command.

```
Syntax: ,autoresponder deny [trigger] [target]
Example: ,autoresponder deny hello bender.py
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-01-19%20191244.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/server/messages/responder.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
