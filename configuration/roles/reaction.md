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
  
</Frame>

## Removing a reaction role

You can remove a reaction role by using the `reactionrole remove` command.

<Tip>
  You can use the `reactionrole list` command to see all reaction roles and their emojis.

  <Frame>
    
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
  
</Frame>

### Removing all reaction roles from the server

You can remove all reaction roles from the server by using the `reactionrole reset` command.

<Warning>
  This **CAN NOT** be undone and will remove **ALL** reaction roles from the
  server.
</Warning>

<Frame>
  
</Frame>

## Setting up a verification system

Reaction roles can be used to create a verification system where members must react to a message to gain access to the server.

<Info>
  In order for this to work, you'll need to create a role that will be assigned
  to members when they react to the message, such as a **Member** role.
</Info>

This section hasn't been written yet. If you'd like to contribute, open a pull request on [Github](https://github.com/ju/docs).