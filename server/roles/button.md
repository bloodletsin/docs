> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/server/roles/button.md).

# Button Roles

## What are button roles?

Button roles are roles that are assigned to members when they click a button on an existing message or embed. They can be useful for letting members choose unique roles or as a way to verify themselves.

## Creating a button role <a href="#creating-a-button-role" id="creating-a-button-role"></a>

You can create multiple button roles for a single message.

{% hint style="warning" %}
Button roles can only be placed on messages & embeds sent by evelina. Learn how to create an embed [**here**](/resources/scripting/embeds.md)!
{% endhint %}

```
Syntax: ;buttonrole add [message] [role] [label] [emoji] [color]
Example: ;buttonrole add .../channels/... member Verify ✅ green
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-01-04%20000538.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
If you don't want a name or an emoji on the button, you can enter "none" as the name/emoji for either of them.
{% endhint %}

## Removing a button role

You can remove a specific button role by using the `buttonrole remove` command.

{% hint style="info" %}
You can use the `buttonrole list` command to see all button roles in your server.
{% endhint %}

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-01-04%20000603.png" alt=""><figcaption></figcaption></figure>

```
Syntax: ;buttonrole remove [button_id]
Example: ;buttonrole remove 5j4ji97J
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-01-04%20000631.png" alt=""><figcaption></figcaption></figure>

## Removing all button roles for a message <a href="#removing-all-button-roles-for-a-message" id="removing-all-button-roles-for-a-message"></a>

Additionally, you can remove all button roles from a message by using the `buttonrole clear` command.

```
Syntax: ;buttonrole clear [message]
Example: ;buttonrole clear .../channels/...
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-01-04%20000656.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/server/roles/button.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
