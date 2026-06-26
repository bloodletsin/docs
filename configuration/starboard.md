> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Starboard

> Allow members to repost interesting messages to a starboard channel.

## What is Starboard?

The starboard is a channel where members can react to messages and after a certain number of reactions, the message will be reposted to the starboard channel.

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/starboard/example.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=cf30b56e540c2350c0101718ebffbe23" width="281" height="234" data-path="images/configuration/starboard/example.png" />
</Frame>

<Info>
  You can create two starboards, both `starboard` and `clownboard` use the
  same structure.
</Info>

## Getting started

Before you run any commands, it's important to use the `starboard unlock` command. Otherwise,
messages will not be reposted to the starboard channel. You can use `starboard lock` to temporarily stop messages from being reposted.

## Setting the starboard channel

You can use the `starboard set` command to set which channel messages will be reposted to.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,starboard set (channel)
  ```

  ```javascript Example theme={null}
  ,starboard set #starboard
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/starboard/set.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=53469a3193ce78d27ea22b915da024d5" width="522" height="176" data-path="images/configuration/starboard/set.png" />
</Frame>

## Ignoring channels, roles, or members

You can ignore certain channels, roles, or members within your server to prevent their messages from appearing on the starboard.

<Info>
  If you no longer want to ignore the channel, role, or member, you can re-run the command. Alternatively, you can run `starboard ignore list` to view all ignored channels, roles, and members.
</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,starboard ignore (role, member, or channel)
  ```

  ```javascript Examples theme={null}
  ,starboard ignore #giveaways
  ,starboard ignore @bryce
  ,starboard ignore @Member
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/starboard/ignore.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=51024d8ddc35d7da5f1b59f435da567b" width="697" height="709" data-path="images/configuration/starboard/ignore.png" />
</Frame>

## Customizing the starboard

### Changing the reaction threshold

You can change the minimum number of reactions a message needs to be reposted.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,starboard threshold (amount)
  ```

  ```javascript Example theme={null}
  ,starboard threshold 3
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/starboard/threshold.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=ab323653043b8d58199568a410187717" width="458" height="171" data-path="images/configuration/starboard/threshold.png" />
</Frame>

### Changing the emoji to watch for

You can set the emoji that members need to react with for a message to be reposted.

<Info>
  By default, this emoji is set as `⭐` for the starboard and `🤡` for the
  clownboard.
</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,starboard emoji (emoji)
  ```

  ```javascript Example theme={null}
  ,starboard emoji 🤩
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/starboard/emoji.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=d1cda589980eb0765a285752dd75484d" width="501" height="202" data-path="images/configuration/starboard/emoji.png" />
</Frame>

### Allowing self-starring messages

You can allow members to star their own messages with the `starboard selfstar` command.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,starboard selfstar (true or false)
  ```

  ```javascript Example theme={null}
  ,starboard selfstar true
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/starboard/selfstar.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=ec439e7549d136d3017d9c492d16846d" width="446" height="170" data-path="images/configuration/starboard/selfstar.png" />
</Frame>

### Customizing the message displayed

You can customize the message that is sent to the starboard channel.

<AccordionGroup>
  <Accordion title="Changing the embed color">
    Use the `starboard color` command to change the color of the embed.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,starboard color (color)
      ```

      ```javascript Example theme={null}
      ,starboard color #cf7c08
      ,starboard color pink
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Toggling the embed timestamp">
    Use the `starboard timestamp` command to toggle the timestamp in the embed.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,starboard timestamp (true or false)
      ```

      ```javascript Example theme={null}
      ,starboard timestamp false
      ```
    </CodeGroup>

    <br />

    <Frame>
      <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/starboard/timestamp.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=a3086b86733ce91361bfe3be0d9112f2" width="277" height="234" data-path="images/configuration/starboard/timestamp.png" />
    </Frame>
  </Accordion>

  <Accordion title="Toggling the message jump URL">
    Use the `starboard jumpurl` command to toggle if the message jump URL is included.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,starboard jumpurl (true or false)
      ```

      ```javascript Example theme={null}
      ,starboard jumpurl false
      ```
    </CodeGroup>

    <br />

    <Frame>
      <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/starboard/jumpurl.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=9b2292563ca518c4969852928c657aa5" width="283" height="232" data-path="images/configuration/starboard/jumpurl.png" />
    </Frame>
  </Accordion>

  <Accordion title="Toggling the message attachments">
    Use the `starboard attachments` command to toggle if attachments are included.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,starboard attachments (true or false)
      ```

      ```javascript Example theme={null}
      ,starboard attachments false
      ```
    </CodeGroup>

    <br />

    <Frame>
      <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/starboard/attachments.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=f4fefc0498668527650ec729bef30229" width="597" height="626" data-path="images/configuration/starboard/attachments.png" />
    </Frame>
  </Accordion>
</AccordionGroup>