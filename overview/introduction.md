> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/overview/introduction.md).

# Introduction

## Guides

{% hint style="info" %}
Server prefix is set to `;` by default. Use `;prefix set (symbol)` to change it for your server.
{% endhint %}

<table data-card-size="large" data-view="cards"><thead><tr><th align="center"></th><th align="center"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td align="center">Security Setup</td><td align="center">Quickly configure your server to use evelina’s advanced moderation system.</td><td><a href="/pages/uFY4GnqQlPvYZntFDLM8">/pages/uFY4GnqQlPvYZntFDLM8</a></td></tr><tr><td align="center">Server Configuration</td><td align="center">Learn how to build embeds and use variables for your server’s configurations</td><td><a href="/pages/cKyl9NsiiqN8Z2gS0UC6">/pages/cKyl9NsiiqN8Z2gS0UC6</a></td></tr><tr><td align="center">Integrations</td><td align="center">Seamlessly integrate your favorite platforms directly into your server through evelina.</td><td><a href="/pages/uIevro7GO2Jd47PoR7iL">/pages/uIevro7GO2Jd47PoR7iL</a></td></tr><tr><td align="center">Embed Scripting</td><td align="center">Learn how to build embeds and use variables for your server’s configurations</td><td><a href="/pages/gnB3eihswUbsz7QJyDfM">/pages/gnB3eihswUbsz7QJyDfM</a></td></tr></tbody></table>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/overview/introduction.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
