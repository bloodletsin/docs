> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Counters

> Create counters in your server

## Overview

Counters allows you to show important info in your server. This can be useful to show your members about significant milestones.

## Adding a counter

You can add a counter using the `counter add` command.

<Info>
  Available counter options are `members`, `users_only`, `bots_only`, `pending_members`,
  `all_channels`, `text_channels`, `voice_channels`, `categories`, `announcement_channels`,
  `staging_channels`, `boosts`, `booster_count` and unix timestamps.
</Info>

<Info>
  Available counter types are `voice` (suggested), `text`, `category`, `announce`,
  and `stage`.
</Info>

<Tip>
  You can create a fun and visble countdown using a UNIX timestamp.
</Tip>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,counter add (option) (type of channel)
  ```

  ```javascript Example theme={null}
  ,counter add members vc
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/miscellaneous/counters/add.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=a8e9c932123564eb81c547b4257e41a4" width="773" height="199" data-path="images/miscellaneous/counters/add.png" />
</Frame>

<br />

## Removing a counter

You can remove a counter using the `counter remove` command.

<Warning>
  After removing counter, you will have to delete the channel (or category) manually.
</Warning>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,counter remove (channel)
  ```

  ```javascript Example theme={null}
  ,counter remove #members
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/miscellaneous/counters/remove.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=260ffdb89e9b8c280968e9f4567e3a74" width="756" height="205" data-path="images/miscellaneous/counters/remove.png" />
</Frame>
