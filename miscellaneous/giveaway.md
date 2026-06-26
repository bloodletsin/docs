> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Giveaway

> Easily create events where members can win prizes.

## Starting a Giveaway

You can start a giveaway with the `giveaway start` command.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,giveaway start <channel> (duration) <winners> (prize)
  ```

  ```javascript Example theme={null}
  ,giveaway start #giveaways 24h 2 Concert Tickets
  ,giveaway start 24h Concert Tickets
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

### Changing the details

You can customize the giveaway with the following commands

<AccordionGroup>
  <Accordion title="Changing the host">
    Use the `giveaway edit host` command to change the giveaway host.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,giveaway edit host (message link) (member)
      ```

      ```javascript Example theme={null}
      ,giveaway edit host .../channels/... @jonathan
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Changing the prize">
    Use the `giveaway edit prize` command to change the giveaway prize.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,giveaway edit prize (message link) (prize)
      ```

      ```javascript Example theme={null}
      ,giveaway edit prize .../channels/... bleh whitelist
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Changing the duration">
    Use the `giveaway edit duration` command to change the duration of the giveaway.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,giveaway edit duration (message link) (duration)
      ```

      ```javascript Example theme={null}
      ,giveaway edit duration .../channels/... 24h
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Changing the amount of winners">
    Use the `giveaway edit winners` command to change the amount of people that can win the giveaway.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,giveaway edit winners (message link) (amount)
      ```

      ```javascript Example theme={null}
      ,giveaway edit winners .../channels/... 3
      ```
    </CodeGroup>
  </Accordion>
</AccordionGroup>

### Customizing the embed

You can customize the giveaway embed with the following commands

<AccordionGroup>
  <Accordion title="Changing the description">
    Use the `giveaway edit description` command to change the giveaway description.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,giveaway edit description (message link) (text)
      ```

      ```javascript Example theme={null}
      ,giveaway edit description .../channels/... Tickets for the Ken Carson concert!
      ```
    </CodeGroup>

    <br />

    <Frame>
      
    </Frame>
  </Accordion>

  <Accordion title="Changing the thumbnail">
    Use the `giveaway edit thumbnail` command to change the giveaway thumbnail.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,giveaway edit thumbnail (message link) (thumbnail)
      ```

      ```javascript Example theme={null}
      ,giveaway edit thumbnail .../channels/... https://bleh.bot/bleh.png
      ```
    </CodeGroup>

    <br />

    <Frame>
      
    </Frame>
  </Accordion>

  <Accordion title="Changing the image">
    Use the `giveaway edit image` command to change the giveaway image.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,giveaway edit image (message link) (image)
      ```

      ```javascript Example theme={null}
      ,giveaway edit image .../channels/... https://bleh.bot/bleh.png
      ```
    </CodeGroup>

    <br />

    <Frame>
      
    </Frame>
  </Accordion>
</AccordionGroup>

### Setting requirements

You can set requirements for the giveaway with the following commands

<AccordionGroup>
  <Accordion title="Setting a required role">
    You can set a required role to enter the giveaway with the following command.
    <Info>If you no longer want to require roles, you can re-run the command without a role.</Info>
    <Warning>You can use multiple roles by separating them with a comma (`,`).</Warning>

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,giveaway edit requiredroles (message link) (roles)
      ```

      ```javascript Example theme={null}
      ,giveaway edit requiredroles .../channels/... @Staff, @Booster
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Setting a required level">
    You can set a required level for the giveaway with the following commands.
    <Warning>This relies on bleh's [leveling system](/configuration/level-rewards), not other bots.</Warning>

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,giveaway edit minlevel (message link) (level)
      ,giveaway edit maxlevel (message link) (level)
      ```

      ```javascript Example theme={null}
      ,giveaway edit minlevel .../channels/... 10
      ,giveaway edit maxlevel .../channels/... 50
      ```
    </CodeGroup>
  </Accordion>
</AccordionGroup>

## Ending a Giveaway

You can end a giveaway early with the `giveaway end` command.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,giveaway end (message link)
  ```

  ```javascript Example theme={null}
  ,giveaway end .../channels/...
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

## Rerolling a Giveaway

You can reroll the winners of a giveaway with the `giveaway reroll` command.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,giveaway reroll (message link)
  ```

  ```javascript Example theme={null}
  ,giveaway reroll .../channels/...
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

## Canceling a Giveaway

You can cancel a giveaway with the `giveaway cancel` command.

<Warning>
  This will not draw any winners and will delete the giveaway message.
</Warning>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,giveaway cancel (message link)
  ```

  ```javascript Example theme={null}
  ,giveaway cancel .../channels/...
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

## Viewing all Giveaways

You can view all giveaways with the `giveaway list` command.

<Info>This will display past and active giveaways.</Info>

<Frame>
  
</Frame>