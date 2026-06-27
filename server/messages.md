> For the complete documentation index, see [llms.txt](https://docs.bleh.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.bot/server/messages.md).

# Messages

<table data-card-size="large" data-view="cards"><thead><tr><th></th><th></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>System Messages</td><td>Automatically send messages when certain member events occur.</td><td><a href="/pages/bKOwlym5Pali2AeMGMZN">/pages/bKOwlym5Pali2AeMGMZN</a></td></tr><tr><td>Auto Responders</td><td>Automatically respond to trigger messages.</td><td><a href="/pages/2Dcsjb6LHyXiBNWWovst">/pages/2Dcsjb6LHyXiBNWWovst</a></td></tr><tr><td>Auto Messages</td><td>Schedule messages to be sent at an interval.</td><td><a href="/pages/ru2OxzDJL7I9ecPkZWaI">/pages/ru2OxzDJL7I9ecPkZWaI</a></td></tr><tr><td>Button Messages</td><td>Response with a message to a button.</td><td><a href="/pages/eYJs77CCgFwH49yH6soR">/pages/eYJs77CCgFwH49yH6soR</a></td></tr></tbody></table>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.bleh.bot/server/messages.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
