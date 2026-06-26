> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Reaction Triggers

> Automatically react to trigger messages.

## Manually reacting to a message

You can use the `reaction` command to react to a message with bleh.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,reaction (message link) (emoji)
  ```

  ```javascript Example theme={null}
  ,reaction .../channels/... 😍
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

## Creating a reaction trigger

You can create a reaction trigger with the `reaction add` command.

<Warning>
  Common words such as `hey` are not allowed as triggers, as they cause heavy
  load on the bot.
</Warning>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,reaction add (emoji) (trigger)
  ```

  ```javascript Example theme={null}
  ,reaction add 😍 jon
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

### Viewing who added a reaction trigger

You can use the `reaction owner` command to view who added a reaction trigger.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,reaction owner (trigger)
  ```

  ```javascript Example theme={null}
  ,reaction owner jon
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

## Removing a reaction trigger

You can remove a reaction trigger with the `reaction remove` command.

<Info>If you're struggling to remove a reaction trigger, refer to the [selection removal](/resources/syntax#removing-entries-via-id).</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,reaction remove (emoji) (trigger)
  ```

  ```javascript Example theme={null}
  ,reaction remove 😍 jon
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

### Removing all reactions for a trigger

You can remove all reactions for a trigger with the `reaction removeall` command.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,reaction removeall (trigger)
  ```

  ```javascript Example theme={null}
  ,reaction removeall jon
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

## Reacting to every message

If you're interested in having reactions on every message, you can use the `reaction messages` command.
This is useful for channels like `#selfies` where messages can be voted on.

<Warning>
  The channel must either be set as `imgonly` or have a slowmode of at least
  **one minute**.
</Warning>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,reaction messages (channel) (up to three emojis)
  ```

  ```javascript Example theme={null}
  ,reaction messages #selfies 😍 😐 🤮
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

### Removing all message reactions

You can use the `reaction messages` command without emojis to remove all reactions.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,reaction messages (channel)
  ```

  ```javascript Example theme={null}
  ,reaction messages #selfies
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

## Related commands

<AccordionGroup>
  <Accordion title="Removing all reaction triggers">
    You can use the `reaction reset` command to remove all reaction triggers.
  </Accordion>

  <Accordion title="Viewing all reaction triggers">
    You can use the `reaction list` command to view all reaction triggers.
  </Accordion>

  <Accordion title="Viewing all channels that are receiving reactions">
    You can use the `reaction messages list` command to view all channels receiving reactions.
  </Accordion>
</AccordionGroup>