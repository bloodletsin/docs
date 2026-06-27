> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/server/roles/vanity.md).

# Vanity Roles

## Getting started

{% hint style="warning" %}
Your server must be **Level 3** with at least **14 boosts** prior to user vanity roles.
{% endhint %}

## Setting the vanity to be monitored

You’ll need to set what vanity you want to monitor. You can do this by using the `;vanity set`command.

{% hint style="info" %}
It’s recommended to prefix the substring with a `/` (e.g. `/evelina`).
{% endhint %}

```
Syntax: ;vanity set [vanity]
Example: ;vanity set /evelina
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-16%20090552.png" alt=""><figcaption></figcaption></figure>

## Setting up roles to reward <a href="#setting-up-roles-to-reward" id="setting-up-roles-to-reward"></a>

You can use the `/vanity role` command to add a vanity reward.

```
// Set Vanity Role
Syntax: /vanity role add [role]
Example: /vanity role add represent

// Remove Vanity Role
Syntax: /vanity role remove 
Example: /vanity role remove
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-16%20090715.png" alt=""><figcaption></figcaption></figure>

### Viewing all roles being rewarded

You can use `;vanity role` list command to view all roles being rewarded.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-16%20090823.png" alt=""><figcaption></figcaption></figure>

## Setting up the award message

You can set a thank you message for when a user advertises your server in their status.

{% hint style="info" %}
The `message` parameter can be raw text or an [embed](https://github.com/EvelinaServices/docs/blob/main/server/roles/broken-reference/README.md) with dynamic [variables](/resources/scripting/variables.md).
{% endhint %}

```
// Set Vanity Message
Syntax: /vanity message [code]
Example: /vanity message {user.mention}, thanks for represent us
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-16%20090923.png" alt=""><figcaption></figcaption></figure>

### Setting where the message is sent

You can use `;vanity channel` command to set where the message is sent.

```
// Set Vanity Channel
Syntax: ;vanity channel set [channel]
Example: ;vanity channel set #support
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-16%20091050.png" alt=""><figcaption></figcaption></figure>

```
// Remove Vanity Channel
Syntax: ;vanity channel remove
Example: ;vanity channel remove
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-16%20091301.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/server/roles/vanity.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
