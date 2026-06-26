> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# System Messages

> Automatically send messages when certain member events occur.

## Commands

There are three system message commands, each with the same subcommands.

* `welcome` - Dispatched whenever a user joins the server.
* `goodbye` - Dispatched whenever a user leaves the server.
* `boost` - Dispatched whenever a user boosts the server.

<Tip>
  The `boost` event is only dispatched if the server has the **Discord System
  Message** enabled or whenever the user receives the **Server Booster** role
  which only occurs once.

  
</Tip>

<Info>
  The following examples use the `welcome` command, but the same syntax is
  applied for the other system message commands.
</Info>

## Creating a system message

You can create a system message with the `welcome add` command.

<Tip>
  The `message` parameter can be raw text or an [embed](/resources/scripting) with dynamic [variables](/resources/scripting/variables).
</Tip>

<Info>
  The `--self_destruct` flag in system messages schedules the message for
  deletion after a specified time, which must be between `6` and `60` seconds.
</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,welcome add (channel) (message) [--self_destruct [6-60]]
  ```

  ```javascript Example theme={null}
  ,welcome add #general welcome to {guild} {user.mention} --self_destruct 30
  ,welcome add #general {embed}$v{message: {user.mention}}$v{description: welcome to {guild.name}}
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

# Removing a system message

You can remove a system message with the `welcome remove` command.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,welcome remove <channel>
  ```

  ```javascript Example theme={null}
  ,welcome remove #joneral
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

## Related commands

<AccordionGroup>
  <Accordion title="Viewing a system message">
    You can use the `welcome view` command to view a system message.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,welcome view (channel)
      ```

      ```javascript Example theme={null}
      ,welcome view #general
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Viewing all system messages">
    You can use the `welcome list` command to view all system messages.
  </Accordion>
</AccordionGroup>