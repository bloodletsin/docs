> For the complete documentation index, see [llms.txt](https://docs.bleh.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.bot/server/messages/button.md).

# Button Messages

## Creating a button message

You can create multiple button messages for a single message.

{% hint style="warning" %}
Button roles can only be placed on messages & embeds sent by bleh. Learn how to create an embed [**here**](https://docs.bleh.bot/resources/scripting/embeds)!
{% endhint %}

```
Syntax: ;buttonmessage add [message] [label] [emoji] [color] [embed]
Example: ;buttonmessage add .../channels/... Rules ✅ green {embed}$v{description: Hello World!}
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-01-04%20001911.png" alt="" width="492"><figcaption></figcaption></figure>

{% hint style="warning" %}
If you don't want a name or an emoji on the button, you can enter "none" as the name/emoji for either of them.
{% endhint %}

## Editing a button response

You can edit a specific button response by using the `buttonmessage edit` command.

{% hint style="info" %}
You can use the `buttonmessage list` command to see all button roles in your server.
{% endhint %}

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-01-04%20002114.png" alt=""><figcaption></figcaption></figure>

```
Syntax: ;buttonmessage edit [button_id] [embed]
Example: ;buttonmessage edit XUrAZTY2 {embed}$v{description: Hello World!}
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-01-04%20002208.png" alt=""><figcaption></figcaption></figure>

## Removing a button response

You can remove a specific button message by using the `buttonmessage remove` command.

```
Syntax: ;buttonmessage remove [button_id]
Example: ;buttonmessage remove XUrAZTY2
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-01-04%20002308.png" alt=""><figcaption></figcaption></figure>

## Removing all button response for a message

Additionally, you can remove all button roles from a message by using the `buttonmessage clear` command.

```
Syntax: ;buttonmessage clear [message]
Example: ;buttonmessage clear .../channels/...
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-01-04%20002431.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.bleh.bot/server/messages/button.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
