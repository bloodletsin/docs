> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Reaction Roles

> Allow your members to assign themselves roles by reacting to a message.

## What are reaction roles?

Reaction roles are roles that are assigned to members when they react to a message. This can be useful for letting members choose unique roles or as a way to verify themselves.

## Creating a reaction role

You can create multiple reaction roles for a single message with a different emoji for each role.

<Info>
  You can find the message link by **right-clicking** or **holding down** on the
  message and selecting **Copy Message Link**.
</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,reactionrole add (message link) (emoji) (role)
  ```

  ```javascript Example theme={null}
  ,reactionrole add .../channels/... ✅ @Member
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/roles/reaction/setting-role.gif?s=07967900a85adb9659d427136bb7b609" width="1082" height="464" data-path="images/configuration/roles/reaction/setting-role.gif" />
</Frame>

## Removing a reaction role

You can remove a reaction role by using the `reactionrole remove` command.

<Tip>
  You can use the `reactionrole list` command to see all reaction roles and their emojis.

  <Frame>
    <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/roles/reaction/list.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=bd5fbd49bef5e2c1e6fbe06cc84345f3" width="390" height="234" data-path="images/configuration/roles/reaction/list.png" />
  </Frame>
</Tip>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,reactionrole remove (message link) (emoji)
  ```

  ```javascript Example theme={null}
  ,reactionrole remove .../channels/... ✅
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/roles/reaction/remove.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=4b0ba248862c3875fa1fa8dd29685b1e" width="583" height="171" data-path="images/configuration/roles/reaction/remove.png" />
</Frame>

### Removing all reaction roles for a message

You can remove all reaction roles for a message with the `reactionrole removeall` command.

<Info>This is different from `reactionrole reset` which removes all reaction roles from the server.</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,reactionrole removeall (message link)
  ```

  ```javascript Example theme={null}
  ,reactionrole removeall .../channels/...
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/roles/reaction/removeall.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=91fbffb073caed2eb91a0626acf108c7" width="606" height="171" data-path="images/configuration/roles/reaction/removeall.png" />
</Frame>

### Removing all reaction roles from the server

You can remove all reaction roles from the server by using the `reactionrole reset` command.

<Warning>
  This **CAN NOT** be undone and will remove **ALL** reaction roles from the
  server.
</Warning>

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/roles/reaction/reset.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=8b0130a7d917a6254cda9beb54682eb7" width="382" height="173" data-path="images/configuration/roles/reaction/reset.png" />
</Frame>

## Setting up a verification system

Reaction roles can be used to create a verification system where members must react to a message to gain access to the server.

<Info>
  In order for this to work, you'll need to create a role that will be assigned
  to members when they react to the message, such as a **Member** role.
</Info>

This section hasn't been written yet. If you'd like to contribute, open a pull request on [Github](https://github.com/ju/docs).