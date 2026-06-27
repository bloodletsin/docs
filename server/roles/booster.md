> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/server/roles/booster.md).

# Booster Roles

## What are booster roles?

Booster roles are unique roles that are given to members which have boosted your server. These roles can be fully customized by the members themselves.

## Setting the base role

In order for the booster roles to work, you must set a base role. All booster roles will be placed under this role.

{% hint style="info" %}
The base role should be a role which is above any roles with a color, otherwise the color won’t be visible due to Discord’s role hierarchy.
{% endhint %}

```
Syntax: ;boosterrole base [role]
Example: ;boosterrole base @---------
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202024-11-19%20223820.png" alt=""><figcaption></figcaption></figure>

## Creating a booster role

You can create a booster role by using the `boosterrole` command itself.

{% hint style="info" %}
The `color` parameter can be a hex code or a color name.
{% endhint %}

```
Syntax: ;boosterrole create [color] [name]
Example: ;boosterrole create #3498DB boss
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_Hv7PERxQWD.png" alt=""><figcaption></figcaption></figure>

## Customizing your booster role

### Changing the name

You can use the `boosterrole name` command to change the name of your booster role.

```
Syntax: ;boosterrole name [name]
Example: ;boosterrole name boss
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_I25XSaDWMz.png" alt=""><figcaption></figcaption></figure>

### Changing the color

You can use the `boosterrole color` command to change the color of your booster role.

```
Syntax: ;boosterrole color [name]
Example: ;boosterrole color #3498DB
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_szBXE2J30Q.png" alt=""><figcaption></figcaption></figure>

### Changing the icon

You can use the `boosterrole icon` command to change the icon of your booster role.

```
Syntax: ;boosterrole icon [emoji]
Example: ;boosterrole icon :cool:
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_GGTEMi6yUn.png" alt=""><figcaption></figcaption></figure>

## Removing your booster role

If you no longer want your booster role, you can use the `boosterrole remove` command.

## Automatically grant a role to boosters

You can reward your boosters with a role upon boosting your server. You can use the `boosterrole award add` command to set this up.

```
Syntax: ;boosterrole award add [role]
Example: ;boosterrole award add gang
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_iQv6PwLzH8.png" alt=""><figcaption></figcaption></figure>

### Removing the role being awarded

You can use the `boosterrole award remove` command to remove the role being awarded.

```
Syntax: ;boosterrole award remove [role]
Example: ;boosterrole award remove gang
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_KL5k3OIF7o.png" alt=""><figcaption></figcaption></figure>

### Viewing the role being awarded

You can use the `boosterrole award list` command to view the roles being awarded.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_6s0ApP7kTD.png" alt=""><figcaption></figcaption></figure>

## Share your boosterrole with other users

In order for the booster roles share to work, you must set a limit. Every user can share then there booster role with this amount of users.

{% hint style="warning" %}
Use `boosterrole share enable` to enable sharing their roles.
{% endhint %}

```
Syntax: ;boosterrole share limit [limit]
Example: ;boosterrole share limit 5
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_OCeuAOPJ2k.png" alt=""><figcaption></figcaption></figure>

### Add a member to share your role

You can use the `boosterrole share add` command to share your role with a member.

```
Syntax: ;boosterrole share add [user]
Example: ;boosterrole share add @bender.py
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_CMcxHqg4z2.png" alt=""><figcaption></figcaption></figure>

### Remove a member from sharing your role

You can use the `boosterrole share remove` command to stop share your role with a member.

```
Syntax: ;boosterrole share remove [user]
Example: ;boosterrole share remove @bender.py
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_DE9M0zOyGz.png" alt=""><figcaption></figcaption></figure>

### List all members you are sharing your role with

You can use the `boosterrole share list` command to view all members your are sharing your role with.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_To1iEUBmIy.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/server/roles/booster.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
