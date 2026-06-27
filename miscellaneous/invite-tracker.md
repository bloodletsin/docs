> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/miscellaneous/invite-tracker.md).

# Invite Tracker

## Getting started <a href="#getting-started" id="getting-started"></a>

The first step to using **Invite Tracker** is to use the `invites enable` command.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_XAoZVKFCoz.png" alt=""><figcaption></figcaption></figure>

## Setting up invite logs <a href="#stacking-reward-roles" id="stacking-reward-roles"></a>

You cann add a logging channel using the `invites logs` command.

```
Syntax: ;invites logs [channel]
Example: ;invites logs #logs
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_Cj6apkPZSS.png" alt=""><figcaption></figcaption></figure>

### Customizing invite logs message

You can change the logs message with the `invites message` command.

{% hint style="info" %}
The `message` parameter can be raw text or an [embed](/resources/scripting/embeds.md) with dynamic [variables](/resources/scripting/variables.md).
{% endhint %}

```
Syntax: ;invites message [message]
Example: ;invites message {inviter.mention} has invited {user.mention} to the server!
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_7SX1UoFlZY.png" alt=""><figcaption></figcaption></figure>

## Setup fake invite tracking

You can change how long a account has to be exist until it count as a real invite with the `invites fake-threshold` command.

{% hint style="info" %}
Default `threshold` is set to **3 days**
{% endhint %}

```
Syntax: ;invites fake-threshold [threshold]
Example: ;invites fake-threshold 5
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_ZFtu0wxtpE.png" alt=""><figcaption></figcaption></figure>

## Setting up roles to reward

You can reward your members with roles when they invite a certain user. You can use the `invites rewards add` command to add a invite reward.

{% hint style="info" %}
If you no longer want to reward a role for a invite amount, you can use the `invites rewards remove` command.
{% endhint %}

{% hint style="warning" %}
If you add new rewards you can use `invites rewards sync` command to ensure that all users get the correct roles based on their invites.
{% endhint %}

```
Syntax: ;invites rewards add [threshold] [role]
Example: ;invites rewards add 5 @Inviter
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_Xh6JkyKG9K.png" alt=""><figcaption></figcaption></figure>

### Stacking reward roles

Stacking roles means that users will keep all the roles they’ve earned when they reach a invite reward, instead of only having the role for their current invite amount. By default, this feature is disabled.

```
Syntax: ;invites rewards stack [option]
Example: ;invites rewards stack on
```

## Related commands

<details>

<summary>View invites from a user</summary>

Use the `invite` command to view a user’s invites.

</details>

<details>

<summary>View all invites create by a user</summary>

Use the `invite code` command to view all invites that create by the given user.

</details>

<details>

<summary>Viewing the invites leaderboard</summary>

Use the `invites leaderboard` subcommand to highets Invite earners in the server.

</details>

<details>

<summary>Viewing the invite rewards</summary>

Use the `invites rewards list` subcommand to view all invite rewards.

</details>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/miscellaneous/invite-tracker.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
