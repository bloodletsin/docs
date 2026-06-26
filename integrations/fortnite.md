> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Fortnite

> Receive shop rotation updates and set reminders for cosmetics.

## Viewing information about a cosmetic

You can use the `fortnite item` command to view information about a cosmetic in Fortnite.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,fortnite item (cosmetic)
  ```

  ```javascript Example theme={null}
  ,fortnite item Toosie Slide
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/integrations/fortnite/item.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=8993fe0b103225ff8543a8d1d0b8d1f8" width="392" height="329" data-path="images/integrations/fortnite/item.png" />
</Frame>

## Receiving reminders for cosmetics

You can use the `fortnite watch` command to be notified when a cosmetic is in the shop.

<Info>If you no longer want to receive reminders for a cosmetic, you can re-run the command.</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,fortnite watch (cosmetic)
  ```

  ```javascript Example theme={null}
  ,fortnite watch Toosie Slide
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/integrations/fortnite/watch.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=9a2a8cd3286b8da950eeb18f2ea67a9f" width="515" height="176" data-path="images/integrations/fortnite/watch.png" />
</Frame>

When the cosmetic is available in the shop, you will receive a message in your DMs.

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/integrations/fortnite/watch/notification.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=cd384913bbfef02fcad036fcef899e93" width="481" height="117" data-path="images/integrations/fortnite/watch/notification.png" />
</Frame>

### Viewing what cosmetics you are watching

You can use the `fortnite watch list` command to view what cosmetics you are watching.

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/integrations/fortnite/watch/list.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=20515fdd9dfc0e25eb71bca03e4b592f" width="292" height="312" data-path="images/integrations/fortnite/watch/list.png" />
</Frame>

## Receiving shop rotation updates

You can use the `fortnite shop` command to receive daily shop rotation updates.

<Info>
  If you no longer want to receive shop rotation updates, you can re-run the
  command without a channel.
</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,fortnite shop (channel)
  ```

  ```javascript Example theme={null}
  ,fortnite shop #updates
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/integrations/fortnite/shop.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=c374eea534d8a28441fa127da5ab5d46" width="507" height="171" data-path="images/integrations/fortnite/shop.png" />
</Frame>

### Notifying a role when the shop updates

You can use the `fortnite shop ping` command to notify a role when the shop updates.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,fortnite shop ping (role)
  ```

  ```javascript Example theme={null}
  ,fortnite shop ping @Updates
  ```
</CodeGroup>

### Letting people vote on the shop

You can use the `fortnite shop voting` command to let people vote on the shop.

<Info>This will add an upvote & downvote reaction to the shop message.</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,fortnite shop voting (on or off)
  ```

  ```javascript Example theme={null}
  ,fortnite shop voting on
  ```
</CodeGroup>