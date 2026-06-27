> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/resources/permissions.md).

# Permissions

| `administrator`       | Allows the user to perform all administrative actions. |
| --------------------- | ------------------------------------------------------ |
| `ban_members`         | Allows the user to ban members.                        |
| `kick_members`        | Allows the user to kick members.                       |
| `manage_guild`        | Allows the user to manage the guild.                   |
| `manage_channels`     | Allows the user to manage channels.                    |
| `manage_roles`        | Allows the user to manage roles.                       |
| `manage_messages`     | Allows the user to manage messages in text channels.   |
| `view_audit_log`      | Allows the user to view the audit log.                 |
| `manage_webhooks`     | Allows the user to manage webhooks.                    |
| `manage_expressions`  | Allows the user to manage emojis.                      |
| `mute_members`        | Allows the user to mute members in voice channels.     |
| `deafen_members`      | Allows the user to deafen members in voice channels.   |
| `move_members`        | Allows the user to move members in voice channels.     |
| `manage_nicknames`    | Allows the user to manage nicknames.                   |
| `mention_everyone`    | Allows the user to mention everyone in messages.       |
| `view_guild_insights` | Allows the user to view guild insights.                |
| `external_emojis`     | Allows the user to use external emojis.                |
| `change_nickname`     | Allows the user to change their nickname.              |


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/resources/permissions.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
