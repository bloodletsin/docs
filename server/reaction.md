> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/server/reaction.md).

# Reaction Triggers

## Manually reacting to a message

You can use the `react` command to react to a message with evelina.

```
Syntax: ;react [message] [emoji]
Example: ;react .../channels/... :f_thumbsup:
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_2c9GoCUeWo.png" alt=""><figcaption></figcaption></figure>

## Creating a reaction trigger

You can create a reaction trigger with the `autoreact add` command.

```
Syntax: ;autoreact add [content]
Example: ;autoreact add panda, :f_thumbsup:
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_aS13udGbMP.png" alt=""><figcaption></figcaption></figure>

## Removing a reaction trigger <a href="#removing-a-reaction-trigger" id="removing-a-reaction-trigger"></a>

You can remove a reaction trigger with the `autoreact remove` command.

```
Syntax: ;autoreact remove [trigger]
Example: ;autoreact remove panda
```

## Reacting to every message

If you’re interested in having reactions on every message, you can use the `autoreact channel add` command. This is useful for channels like `#selfies` where messages can be voted on.

{% hint style="warning" %}
The channel must either be set as `imgonly` or have a slowmode of at least **one minute**.
{% endhint %}

```
Syntax: ;autoreact channel add [channel] [reactions]
Example: ;autoreact channel add #general 😍 😐 🤮
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_Qu9GpzFzaz.png" alt=""><figcaption></figcaption></figure>

### Removing all message reactions <a href="#removing-all-message-reactions" id="removing-all-message-reactions"></a>

You can use the `autoreact channel remove` command without emojis to remove all reactions.

```
Syntax: ;autoreact channel remove [channel]
Example: ;autoreact channel remove #general
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_s8kKLqO2A2.png" alt=""><figcaption></figcaption></figure>

## Related commands

<details>

<summary>Removing all reaction triggers</summary>

You can use the `autoreact reset` or `autoreact channel reset` command to remove all reaction triggers.

</details>

<details>

<summary>Viewing all reaction triggers</summary>

You can use the `autoreact list` command to view all reaction triggers.

</details>

<details>

<summary>Viewing all channels that are receiving reactions</summary>

You can use the `autoreact channel list` command to view all channels receiving reactions.

</details>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/server/reaction.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
