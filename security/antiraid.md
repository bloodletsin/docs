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
  <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antiraid/massjoin.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=5a0ef54c0b01df31d4d840e7d4a954ec" width="661" height="190" data-path="images/security/antiraid/massjoin.png" />
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
  <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antiraid/avatar.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=b3e366950ba2a00238095c9d2a9c53b5" width="521" height="172" data-path="images/security/antiraid/avatar.png" />
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
  <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antiraid/age.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=3c68e3976fa9fee11fc1d269c17434ee" width="663" height="194" data-path="images/security/antiraid/age.png" />
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
  <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antiraid/whitelist.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=f6c055f770a392c9cb8b8e82c2b10406" width="545" height="175" data-path="images/security/antiraid/whitelist.png" />
</Frame>

## Viewing the antiraid configuration

You can use the `antiraid config` command to view the current antiraid configuration.

<Frame>
  <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antiraid/config.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=d33fdc88289eff3c9920d740cb672952" width="452" height="331" data-path="images/security/antiraid/config.png" />
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