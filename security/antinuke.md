> For the complete documentation index, see [llms.txt](https://docs.bleh.rest/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.rest/security/antinuke.md).

# Antinuke

## Information



Antinuke is triggered by a threshold set **per user**.

Your antinuke should **never** have to be higher than 5. Antinuke will not work as well if it's threshold is set high. We recommend a threshold between 1 and 5.

## Parameters

| Name       | Description                   |
| ---------- | ----------------------------- |
| threshold  | Threshold to trigger antinuke |
| punishment | Action to be taken on trigger |
| time       | Threshold for account age     |



## Punishments

Click the following to view all antinuke punishments available:


[Punishments](/resources/punishments.md)


## Admins & Whitelisted <a href="#admins-and-whitelisted" id="admins-and-whitelisted"></a>

You can whitelist members from triggering antinuke by using `antinuke whitelist [user]`.

You can also grant antinuke admin to a user, which allows them to modify antinuke settings. You can do this by using `[prefix] antinuke admin [user]`. Only give this to people you trust.



## Antinuke Logs <a href="#antinuke-logs" id="antinuke-logs"></a>

You can set a channel to send antinuke logs by using `antinuke logs`. Whenever antinuke is triggered, a message will be sent to that channel. It is recommended that you set this up.

## Antinuke Recommended Configuration

If you don't know how to configure your Antinuke, here is our recommended config for the Antinuke module.

```
// Role Config
antinuke rolecreate enable 3 strip
antinuke roledelete enable 1 strip
antinuke editrole enable ban
antinuke giverole enable strip

// Channel Config
antinuke channelcreate enable 3 strip
antinuke channeldelete enable 1 strip

// Role Moderation
antinuke kick enable 3 kick
antinuke ban enable 3 kick
antinuke botadd enable strip
```


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.bleh.rest/security/antinuke.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.