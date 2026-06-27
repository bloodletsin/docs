> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Logging

> Log events in your server.

## Overview

Logging allows you to log events in your server. This can be useful for keeping track of what's happening in your server.

## Adding a logging event

You can add a logging event using the `log add` command.

<Info>
  Available logging events are `messages`, `members`, `roles`, `channels`,
  `invites`, `emojis` and `voice`.
</Info>

<Warning>
  Do not delete the webhook that bleh creates in your logging channels!
</Warning>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,log add (channel) (event)
  ```

  ```javascript Example theme={null}
  ,log add #logs messages
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/logging/add.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=b6f2e7dfe8d6a2f4f7cc1faa5882902a" width="407" height="155" data-path="images/configuration/logging/add.png" />
</Frame>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/logging/example.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=e74f31d984d2b34b04f12ff41357d68c" width="416" height="389" data-path="images/configuration/logging/example.png" />
</Frame>

## Removing a logging event

You can remove a logging event using the `log remove` command.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,log remove (channel) (event)
  ```

  ```javascript Example theme={null}
  ,log remove #logs messages
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/logging/remove.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=276266440470159494b486f90f7ce621" width="435" height="156" data-path="images/configuration/logging/remove.png" />
</Frame>

<Tip>
  You can leave the event parameter empty to add or remove all logging events
  from a channel.
</Tip>

## Ignoring a member or channel

You can ignore and unignore a member or channel from being logged using the `log ignore` command.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,log ignore (member or channel)
  ```

  ```javascript Example theme={null}
  ,log ignore @jonathan
  ,log ignore #staff-chat
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/logging/ignore.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=496feec888e9132ef2da48c0b819f8ea" width="370" height="318" data-path="images/configuration/logging/ignore.png" />
</Frame>

## Related commands

<Info>
  You can use the `log ignore list` command to view all ignored members and
  channels.
</Info>
