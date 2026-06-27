> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/server/roles/reaction.md).

# Reaction Roles

## What are reaction roles?

Reaction roles are roles that are assigned to members when they react to a message. This can be useful for letting members choose unique roles or as a way to verify themselves.

## Creating a reaction role <a href="#creating-a-reaction-role" id="creating-a-reaction-role"></a>

You can create multiple reaction roles for a single message with a different emoji for each role.

{% hint style="info" %}
You can find the message link by **right-clicking** or **holding down** on the message and selecting **Copy Message Link**.
{% endhint %}

```
Syntax: ;reactionrole add [message] [emoji] [role]
Example: ;reactionrole add .../channels/... :skull: dead chat
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_xplsTENrss.png" alt=""><figcaption></figcaption></figure>

## Removing a reaction role <a href="#removing-a-reaction-role" id="removing-a-reaction-role"></a>

You can remove a reaction role by using the `reactionrole remove` command.

{% hint style="info" %}
You can use the `reactionrole list` command to see all reaction roles and their emojis.
{% endhint %}

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_XnbLC7ueMv.png" alt="" width="290"><figcaption></figcaption></figure>

```
Syntax: ;reactionrole remove [message] [emoji]
Example: ;reactionrole remove .../channels/... :skull:
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_3HAiA4qEQq.png" alt=""><figcaption></figcaption></figure>

### Removing all reaction roles for a message <a href="#removing-all-reaction-roles-for-a-message" id="removing-all-reaction-roles-for-a-message"></a>

You can remove all reaction roles for a message with the `reactionrole removeall` command.

{% hint style="info" %}
This is different from `reactionrole clear` which removes all reaction roles from the server.
{% endhint %}

```
Syntax: ;reactionrole removeall [message]
Example: ;reactionrole removeall .../channels/...
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_yjAT9xruhv.png" alt=""><figcaption></figcaption></figure>

### Removing all reaction roles from the server

You can remove all reaction roles from the server by using the `reactionrole clear` command.

{% hint style="warning" %}
This **CAN NOT** be undone and will remove **ALL** reaction roles from the server.
{% endhint %}

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_Lk04LuXR1v.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/server/roles/reaction.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
