> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/security/join-gate.md).

# Join Gate

## Configuring the antiraid system

### Preventing mass joins <a href="#preventing-mass-joins" id="preventing-mass-joins"></a>

This module will trigger when the number of accounts joining the server exceeds the threshold within a short time frame.

```
Syntax: ;antiraid massjoin enable [punishment] [threshold]
Example: ;antiraid massjoin enable ban 3
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-26%20022438.png" alt=""><figcaption></figcaption></figure>

### Requiring an avatar <a href="#requiring-an-avatar" id="requiring-an-avatar"></a>

This module will trigger when an account joins the server without an avatar.

```
Syntax: ;antiraid avatar enable [punishment]
Example: ;antiraid avatar enable ban
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-26%20022541.png" alt=""><figcaption></figcaption></figure>

### Setting a minimum account age

This module will trigger when an account joins the server that is younger than the specified age.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-26%20022658.png" alt=""><figcaption></figcaption></figure>

### Exempting accounts from the antiraid <a href="#exempting-accounts-from-the-antiraid" id="exempting-accounts-from-the-antiraid"></a>

You can exempt accounts from the antiraid with the `antiraid whitelist` command.

{% hint style="info" %}
You can use the `antiraid whitelist view` command to view all whitelisted accounts.
{% endhint %}

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-26%20022814.png" alt=""><figcaption></figcaption></figure>

## Viewing the antiraid configuration <a href="#viewing-the-antiraid-configuration" id="viewing-the-antiraid-configuration"></a>

You can use the `antiraid config` command to view the current antiraid configuration.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-26%20022847.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/security/join-gate.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
