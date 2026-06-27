> For the complete documentation index, see [llms.txt](https://docs.bleh.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.bot/security/auto-moderation/words.md).

# Words

## Enable Word Filter

This module will trigger when a user try to send invites in your chat.

```
Syntax: ;automod words enable 
Example: ;automod words enable 
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20211623.png" alt=""><figcaption></figcaption></figure>

## Customize Bad Words

With this commands you can add or remove bad words.

```
Syntax: ;automod words add [word]
Example: ;automod words add word
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20211818.png" alt=""><figcaption></figcaption></figure>

```
Syntax: ;automod words remove [word]
Example: ;automod words remove word
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20211833.png" alt=""><figcaption></figcaption></figure>

```
Syntax: ;automod words list 
Example: ;automod words list
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20212023.png" alt=""><figcaption></figcaption></figure>

## Customize Word Filter

You can customize things like, timeout duration, customize punishment message or logging channel.

```
Syntax: ;automod words timeout [time]
Example: ;automod words timeout 1d
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20212143.png" alt=""><figcaption></figcaption></figure>

```
Syntax: ;automod words message [message]
Example: ;automod words message You are not allowed to send invite links here.
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20212208.png" alt=""><figcaption></figcaption></figure>

```
Syntax: ;automod words logs [channel]
Example: ;automod words logs #logs
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20212238.png" alt=""><figcaption></figcaption></figure>

## Whitelist Channel, Category or Role

With this command you can ignore someone from the bad word filter system.

```
Syntax: ;automod words ignore add [target]
Example: ;automod words  ignore add #channel
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20212615.png" alt=""><figcaption></figcaption></figure>

```
Syntax: ;automod words ignore remove [target]
Example: ;automod words ignore remove #channel
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20212641.png" alt=""><figcaption></figcaption></figure>

```
Syntax: ;automod words ignore list
Example: ;automod words ignore list
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-27%20212733.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.bleh.bot/security/auto-moderation/words.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
