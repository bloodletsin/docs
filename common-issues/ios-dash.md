> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/common-issues/ios-dash.md).

# iOS Dash

If evelina is responding with a different response for a flag than the one you specified, make sure you’re using the correct `--` instead of `—`. **iOS** devices automatically convert two dashes into a single long dash, which can cause issues with commands that require flags.

You can solve this issue by disabling the **Smart Punctuation** feature on your **iOS** device. To do this, go to **Settings** -> **General** -> **Keyboard** and disable the **Smart Punctuation** option.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/smart-punctuation.png" alt="" width="188"><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/common-issues/ios-dash.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
