> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/miscellaneous/webhook.md).

# Webhook

## What is a webhook? <a href="#what-is-a-webhook" id="what-is-a-webhook"></a>

A webhook is a way to post a message with a custom username and avatar to a channel.

{% hint style="info" %}
Webhooks support [embeds](/resources/scripting/embeds.md) with dynamic [variables](/resources/scripting/variables.md).
{% endhint %}

```
Syntax: ;webhook create [channel] [name]
Example: ;webhook create #welcome evelina
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_kiAhPgu5Pe.png" alt=""><figcaption></figcaption></figure>

### Customizing the webhook <a href="#customizing-the-webhook" id="customizing-the-webhook"></a>

If you want to change the webhook’s username or avatar, you can use the `webhook edit` command.

```
Syntax: ;webhook edit name [code] [name]
Example: ;webhook edit name bZYdgLvu evelina
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_nSA8AeM6lr.png" alt=""><figcaption></figcaption></figure>

```
Syntax: ;webhook edit avatar [code] [url]
Example: ;webhook edit avatar bZYdgLvu https://evelina.bot/icon.png
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_n2UodoMHO7.png" alt=""><figcaption></figcaption></figure>

## Sending a message <a href="#sending-a-message" id="sending-a-message"></a>

After creating a webhook, you can use the `webhook send` command to send a message.

{% hint style="info" %}
If you’ve forgotten the identifier, you can use the `webhook list` command to view all webhooks.
{% endhint %}

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_XfPoxQnxPa.png" alt=""><figcaption></figcaption></figure>

### Editing the message <a href="#editing-the-message" id="editing-the-message"></a>

You can use the `webhook update` command to edit a message sent by a webhook.

```
Syntax: ;webhook update [message] [script]
Example: ;webhook update .../channels.../ hello world
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_KHTwSx2qPN.png" alt=""><figcaption></figcaption></figure>

## Related commands <a href="#related-commands" id="related-commands"></a>

<details>

<summary>Deleting a webhook</summary>

You can use the `webhook delete` command to delete a webhook.

```
Syntax: ;webhook delete [code]
Example: ;webhook delete bZYdgLvu
```

</details>

<details>

<summary>Viewing all webhooks</summary>

You can use the `webhook list` command to view all webhooks.

</details>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/miscellaneous/webhook.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
