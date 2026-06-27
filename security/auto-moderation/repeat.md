> For the complete documentation index, see [llms.txt](https://docs.bleh.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.bot/security/auto-moderation/repeat.md).

# Repeat

## Enable Repeat Filter

This module will trigger when a user repeat a certain amout of message in your chat.

```
Syntax: ;automod repeat enable
Example: ;automod repeat enable
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20213141.png" alt=""><figcaption></figcaption></figure>

## Customize Repeat Filter

You can customize things like, timeout duration, message per 10 seconds or if a message should be sent on punishment.

```
Syntax: ;automod repeat timeout [time]
Example: ;automod repeat timeout 1h
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20213200.png" alt=""><figcaption></figcaption></figure>

```
Syntax: ;automod repeat rate [rate]
Example: ;automod repeat rate 5
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20213218.png" alt=""><figcaption></figcaption></figure>

```
Syntax: ;automod repeat message [option]
Example: ;automod repeat message on
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20213238.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.bleh.bot/security/auto-moderation/repeat.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
