> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Auto Messages

> Schedule messages to be sent at an interval.

<Warning>
  You can only have **one** auto message per channel, and the interval must be
  at least **10 minutes**.
</Warning>

## Creating an auto message

You can create an auto message with the `timer add` command.

<Info>
  The `interval` parameter must use the proper format, you can learn more
  [here](/resources/syntax#formatting-a-duration).
</Info>

<Tip>
  The `message` parameter can be raw text or an [embed](/resources/scripting) with dynamic [variables](/resources/scripting/variables).
</Tip>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,timer add (channel) (interval) (message)
  ```

  ```javascript Example theme={null}
  ,timer add #general 2h hey sexy ass people
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/messages/timer/add.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=07bbdc815e1eef4e13a85546be023e8c" width="613" height="226" data-path="images/configuration/messages/timer/add.png" />
</Frame>

## Removing an auto message

You can remove an auto message with the `timer remove` command.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,timer remove (channel)
  ```

  ```javascript Example theme={null}
  ,timer remove #general
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/messages/timer/remove.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=1c91b147a73d25c0ca69d5a47775f3ff" width="483" height="174" data-path="images/configuration/messages/timer/remove.png" />
</Frame>

## Related commands

<AccordionGroup>
  <Accordion title="Viewing an auto messages">
    You can use the `timer view` command to view auto message.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,timer view (channel)
      ```

      ```javascript Example theme={null}
      ,timer view #general
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Viewing all auto messages">
    You can use the `timer list` command to view all auto messages.
  </Accordion>
</AccordionGroup>