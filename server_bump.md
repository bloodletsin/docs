> For the complete documentation index, see [llms.txt](https://docs.bleh.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.bot/server/bump.md).

# Bump Reminder

## Why use bump reminders?

Receiving reminders to bump your server on **DISBOARD** can help you increase your server’s visibility and attract new members. You can set up the **DISBOARD** bot by clicking [here](https://discord.com/oauth2/authorize?scope=identify+guilds+guilds.join\&response_type=code\&approval_prompt=auto\&client_id=302050872383242240\&redirect_uri=https%3A%2F%2Fdisboard.org%2Fsite%2Foauth-callback).

## Setting up bump reminders <a href="#setting-up-bump-reminders" id="setting-up-bump-reminders"></a>

Once you’ve invited the **DISBOARD** bot, you can set up bump reminders by setting the channel where you want to receive reminders to run `/bump` every **two hours**.

```
;bumpreminder enable
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202025-01-03%20220420.png" alt=""><figcaption></figcaption></figure>

## Customizing bump reminders

### Changing the reminder message <a href="#changing-the-reminder-message" id="changing-the-reminder-message"></a>

You can change the reminder message with the `bumpreminder reminder` command. This is the message that will be sent every **two hours** when it’s time to `/bump` the server.

{% hint style="info" %}
The `message` parameter can be raw text or an [embed](/resources/scripting/embeds.md) with dynamic [variables](/resources/scripting/variables.md).
{% endhint %}

```
Syntax: ;bumpreminder reminder [code]
Example: ;bumpreminder reminder Bump the server using **/bump**
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Discord_psbNEIiamL.png" alt=""><figcaption></figcaption></figure>

### Changing the thank you message <a href="#changing-the-thank-you-message" id="changing-the-thank-you-message"></a>

You can change the message which will be sent after bumping the server with the `bumpreminder thankyou` command.

{% hint style="info" %}
The `message` parameter can be raw text or an [embed](/resources/scripting/embeds.md) with dynamic [variables](/resources/scripting/variables.md).
{% endhint %}

```
Syntax: ;bumpreminder thankyou [code]
Example: ;bumpreminder thankyou Thanks, {user.mention}
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Discord_IVTSwSnfBf.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.bleh.bot/server/bump.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.