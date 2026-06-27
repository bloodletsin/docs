> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/security/auto-moderation.md).

# Auto Moderation

<table data-card-size="large" data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td><strong>Invite</strong></td><td>Prevent members from sending invite links</td><td><a href="/pages/yVsNUcGeRfGnukgsFais">/pages/yVsNUcGeRfGnukgsFais</a></td></tr><tr><td><strong>Words</strong></td><td>Enable protection against blacklisted words</td><td><a href="/pages/uZz9BFsNBqN76kBzAXjV">/pages/uZz9BFsNBqN76kBzAXjV</a></td></tr><tr><td><strong>Spamming</strong></td><td>Enable protection against message spamming</td><td><a href="/pages/gaw77gjAgZYvM3YhrwPY">/pages/gaw77gjAgZYvM3YhrwPY</a></td></tr><tr><td><strong>Repeat</strong></td><td>Enable protection against message repeating</td><td><a href="/pages/jLmAkvVI1emkebSRPPSE">/pages/jLmAkvVI1emkebSRPPSE</a></td></tr></tbody></table>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/security/auto-moderation.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
