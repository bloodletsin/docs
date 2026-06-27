> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Vanity Roles

> Reward your members for advertising your server in their status.

## Getting started

This feature uses a dedicated bot due to some limitations with the main bleh bot. You can invite the dedicated bot by clicking [here](https://discord.com/oauth2/authorize?client_id=996638412675227668\&permissions=8\&scope=bot%20applications.commands).

<Warning>
  Your server must be **Level 3** with at least **14 boosts** prior to inviting
  the dedicated bot.
</Warning>

<Info>
  All commands are **slash commands** and can be accessed by typing `/vanity` in
  a text channel.
</Info>

## Setting the vanity to be monitored

You'll need to set what vanity you want to monitor. You can do this by using the `/vanity set` command.

<Tip>It's recommended to prefix the substring with a `/` (e.g. `/bleh`).</Tip>

<CodeGroup>
  ```javascript Syntax theme={null}
  /vanity set (substring)
  ```

  ```javascript Example theme={null}
  /vanity set /bleh
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/roles/vanity/set-substring.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=7549afa286423548397987e58ad0b8fd" width="419" height="125" data-path="images/configuration/roles/vanity/set-substring.png" />
</Frame>

## Setting up roles to reward

You can use the `/vanity role add` command to add a vanity reward.

<Info>
  If you no longer want to reward a role for a vanity, you can use the `/vanity
      role remove` command.
</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  /vanity role add (role)
  /vanity role remove (role)
  ```

  ```javascript Example theme={null}
  /vanity role add @Vanity
  /vanity role remove @Vanity
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/roles/vanity/setting-roles.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=076d214a53517fc11473463f63d9e2f8" width="430" height="257" data-path="images/configuration/roles/vanity/setting-roles.png" />
</Frame>

### Viewing all roles being rewarded

You can use the `/vanity role list` command to view all roles being rewarded.

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/roles/vanity/role-list.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=0745a85bef98bef3950f8aa747c716d2" width="349" height="219" data-path="images/configuration/roles/vanity/role-list.png" />
</Frame>

## Setting up the award message

You can set a thank you message for when a user advertises your server in their status.

<Info>
  The `message` parameter can be raw text or an [embed](/resources/scripting)
  with dynamic [variables](/resources/scripting/variables).
</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  /vanity message (message)
  ```

  ```javascript Example theme={null}
  /vanity message thank you {user.mention}
  /vanity message {embed}$v{message: {user.mention}}$v{description: thank you for advertising our server!}
  ```
</CodeGroup>

### Setting where the message is sent

You can use the `/vanity award channel` command to set where the message is sent.

<CodeGroup>
  ```javascript Syntax theme={null}
  /vanity award channel (channel)
  ```

  ```javascript Example theme={null}
  /vanity award channel #general
  ```
</CodeGroup>
