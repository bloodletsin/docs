> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Join Gate

> Prevent automated accounts from joining your server.

## Configuring the antiraid system

### Preventing mass joins

This module will trigger when the number of accounts joining the server exceeds the threshold within a short time frame.

<Warning>
  Whenever the threshold is reached, the server will be placed in a raid state.
  This will temporarily disable intensive events which bleh dispatches, such as
  **welcome** and **goodbye** messages.
</Warning>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,antiraid massjoin (on or off) [--threshold (number)] [--do (action)] [--lock (true | false)] [--punish (true | false)]
  ```

  ```javascript Example theme={null}
  ,antiraid massjoin on --threshold 5 --do ban --lock true --punish true
  ```
</CodeGroup>

<br />

<AccordionGroup>
  <Accordion title="Threshold">
    The threshold is the number of accounts that can join the server within the time frame.
    <Info>It's recommended to keep the threshold between `5` and `10` to stay safe.</Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      --threshold (number)
      ```

      ```javascript Example theme={null}
      --threshold 5
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Punishment">
    The action which will be taken when the threshold is reached.
    <Info>Available actions are `ban` and `kick`.</Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      --do (action)
      ```

      ```javascript Example theme={null}
      --do ban
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Lock channels">
    Whether to lock all channels when the threshold is reached.

    <CodeGroup>
      ```javascript Syntax theme={null}
      --lock (true | false)
      ```

      ```javascript Example theme={null}
      --lock true
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Punish new accounts">
    Whether to punish new accounts that join the server.

    <CodeGroup>
      ```javascript Syntax theme={null}
      --punish (true | false)
      ```

      ```javascript Example theme={null}
      --punish true
      ```
    </CodeGroup>
  </Accordion>
</AccordionGroup>

<Frame>
  
</Frame>

### Requiring an avatar

This module will trigger when an account joins the server without an avatar.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,antiraid avatar (on or off) [--do (action)]
  ```

  ```javascript Example theme={null}
  ,antiraid avatar on --do kick
  ```
</CodeGroup>

<br />

<AccordionGroup>
  <Accordion title="Punishment">
    The action which will be taken when the threshold is reached.
    <Info>Available actions are `ban` and `kick`.</Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      --do (action)
      ```

      ```javascript Example theme={null}
      --do ban
      ```
    </CodeGroup>
  </Accordion>
</AccordionGroup>

<Frame>
  
</Frame>

### Setting a minimum account age

This module will trigger when an account joins the server that is younger than the specified age.

<Info>
  The `threshold` flag is the numbers of days for an account to be considered
  old enough.
</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,antiraid age (on or off) [--threshold (number)] [--do (action)]
  ```

  ```javascript Example theme={null}
  ,antiraid age on --threshold 7 --do ban
  ```
</CodeGroup>

<br />

<AccordionGroup>
  <Accordion title="Threshold">
    The threshold is the number of accounts that can join the server within the time frame.
    <Info>It's recommended to keep the threshold between `5` and `10` to stay safe.</Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      --threshold (number)
      ```

      ```javascript Example theme={null}
      --threshold 5
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Punishment">
    The action which will be taken when the threshold is reached.
    <Info>Available actions are `ban` and `kick`.</Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      --do (action)
      ```

      ```javascript Example theme={null}
      --do ban
      ```
    </CodeGroup>
  </Accordion>
</AccordionGroup>

<Frame>
  
</Frame>

### Exempting accounts from the antiraid

You can exempt accounts from the antiraid with the `antiraid whitelist` command.

<Info>You can use the `antiraid whitelist view` command to view all whitelisted accounts.</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,antiraid whitelist (user)
  ```

  ```javascript Example theme={null}
  ,antiraid whitelist @jonathan
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

## Viewing the antiraid configuration

You can use the `antiraid config` command to view the current antiraid configuration.

<Frame>
  
</Frame>

## What to do after a raid

<Steps>
  <Step title="Cleaning up">
    After a raid, it's recommended to clean up the server by removing all the accounts that joined during the raid, you can do this with the `recentban` and `raid` commands.

    <Info>
      The `duration` parameter must use the proper format, you can learn more
      [here](/resources/syntax#formatting-a-duration).
    </Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,recentban (amount) <reason>
      ,raid (duration) (kick or ban) <reason>
      ```

      ```javascript Example theme={null}
      ,recentban 50 // Bans the last 50 accounts that joined the server
      ,raid 2h ban // Bans all accounts that joined the server in the last 2 hours
      ```
    </CodeGroup>
  </Step>

  <Step title="Disabling the raid state">
    After the raid is over, you can disable the raid state with the `antiraid state` command, this will re-enable events, unlock channels, and allow accounts to join the server.
  </Step>
</Steps>