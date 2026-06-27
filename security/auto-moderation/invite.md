> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/security/auto-moderation/invite.md).

# Invite

## Enable Invite Filter

This module will trigger when a user try to send invites in your chat.

```
Syntax: ;automod invites enable 
Example: ;automod invites enable 
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20210254.png" alt=""><figcaption></figcaption></figure>

## Customize Invite Filter

You can customize things like, timeout duration, customize punishment message or logging channel.

```
Syntax: ;automod invites timeout [time]
Example: ;automod invites timeout 1d
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20210650.png" alt=""><figcaption></figcaption></figure>

```
Syntax: ;automod invites message [message]
Example: ;automod invites message You are not allowed to send invite links here.
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20210724.png" alt=""><figcaption></figcaption></figure>

```
Syntax: ;automod invites logs [channel]
Example: ;automod invites logs #logs
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20210815.png" alt=""><figcaption></figcaption></figure>

## Whitelist Channel, Category or Role

With this command you can ignore someone from the invites filter system.

```
Syntax: ;automod invites ignore add [target]
Example: ;automod invites ignore add #channel
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20211049.png" alt=""><figcaption></figcaption></figure>

```
Syntax: ;automod invites ignore remove [target]
Example: ;automod invites ignore remove #channel
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20211322.png" alt=""><figcaption></figcaption></figure>

```
Syntax: ;automod invites ignore list
Example: ;automod invites ignore list
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20211422.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/security/auto-moderation/invite.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
