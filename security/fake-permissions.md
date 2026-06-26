> For the complete documentation index, see [llms.txt](https://docs.bleh.rest/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.rest/security/fake-permissions.md).

# Fake Permissions

## Why use fake permissions?

Fake permissions negate the possibility of a rogue moderator using a script which floods the **Discord API** and mass bans all members, or any other harmful action. It’s a security measure which ensures that your server can’t be nuked whatsoever.

## How do fake permissions work?

When a moderator is given fake permissions, such as `ban_members`, they will be able to use the `ban` command with **bleh**, but they won’t be able to use the native **Discord** ban feature.

## Getting command permissions

You can locate the required permissions for a command with `;help (command)`



## Setting up fake permissions



<details>

<summary>Granting fake permissions to a role</summary>

Use the `fakepermissions add` command to grant a fake permission to a role.

```
Syntax: ;fakepermissions add [role] [permission]
Example: ;fakepermissions add mod manage_messages
```

</details>

<details>

<summary>Revoking fake permissions from a role</summary>

Use the `fakepermissions remove` command to revoke a fake permission from a role.

```
Syntax: ;fakepermissions remove [role] [permission]
Example: ;fakepermissions remove mod manage_messages
```

</details>

<details>

<summary>Clear all fake permissions from a role</summary>

Use the `fakepermissions clear` command to revoke all fake permission from a role.

```
Syntax: ;fakepermissions clear [role]
Example: ;fakepermissions clear mod
```

</details>

<details>

<summary>Viewing fake permissions</summary>

Use the `fakepermissions list` command to view all fake permissions.

```
Syntax: ;fakepermissions list [role]
Example: ;fakepermissions list mod
```

</details>

<details>

<summary>Revoking all fake permissions</summary>

Use the `fakepermissions reset` command to reset all fake permissions.

</details>

## Recommended Configuration




---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.bleh.rest/security/fake-permissions.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.