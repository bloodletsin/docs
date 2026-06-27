> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# VoiceMaster

> Create temporary voice channels which can be customized to your liking.

## Getting started

The first step to using **VoiceMaster** is to use the `voicemaster setup` command.

<Tip>The created channels can be moved and renamed to your liking.</Tip>

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/voicemaster/setup.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=5eb08ffd86a00f29faff44ec1a71e677" width="651" height="213" data-path="images/configuration/voicemaster/setup.png" />
</Frame>

### What is the interface channel?

The `#interface` channel will contain an embed with buttons that allow members to customize their temporary voice channel. This channel should be locked to keep the embed message at the top of the channel.

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/voicemaster/interface.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=f0f770191a38be527cef9735fe4673e1" width="567" height="488" data-path="images/configuration/voicemaster/interface.png" />
</Frame>

### What is the Join to Create channel?

The **Join to Create** channel is where members will join to create their temporary voice channel. This channel is required for the **VoiceMaster** system to work.

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/voicemaster/join-to-create.gif?s=09bee0cbd0f373bc8ca7d540dd962c85" width="262" height="204" data-path="images/configuration/voicemaster/join-to-create.gif" />
</Frame>

## Customizing new voice channels

You can customize what the temporary voice channels look like when they're created.

The following commands are subcommands of the `voicemaster default` command.

<AccordionGroup>
  <Accordion title="Redirecting voice channels">
    Redirect voice channels to a specific category.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,voicemaster category (category)
      ```

      ```javascript Example theme={null}
      ,voicemaster category Voice Channels
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Setting the default channel name">
    <Info>The name can use the `{user}`, `{user.name}` and `{user.display_name}` variables.</Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,voicemaster default name (name)
      ```

      ```javascript Example theme={null}
      ,voicemaster default name {user.display_name}'s vc
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Setting the default channel bitrate">
    <Info>The bitrate must be between `8` and `384`.</Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,voicemaster default bitrate (kbps)
      ```

      ```javascript Example theme={null}
      ,voicemaster default bitrate 384
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Setting the default channel region">
    <Info>
      The region must be one of the following
      <br />`brazil`, `hongkong`, `india`, `japan`, `rotterdam`, `russia`, `singapore`, `south-korea`, `southafrica`, `sydney`, `us-central`, `us-east`, `us-south`, `us-west`
    </Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,voicemaster default region (region)
      ```

      ```javascript Example theme={null}
      ,voicemaster default region russia
      ```
    </CodeGroup>
  </Accordion>
</AccordionGroup>

## Granting a role to members

You can assign a role that members receive when they join a temporary voice channel, which is automatically removed when they leave. This is helpful if you want your `#interface` channel to be visible only to members currently in a temporary voice channel.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,voicemaster join role (role)
  ```

  ```javascript Example theme={null}
  ,voicemaster join role @in bryce's vc
  ```
</CodeGroup>

### Setting up the permissions

If you're interested in making your `#interface` channel only visible to members inside a temporary voice channel, you would need to set the permissions accordingly.

You would need to deny the **View Channel** permission for the `@everyone` role and allow the **View Channel** permission for the role you set in the previous step.

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/voicemaster/interface-permissions.gif?s=d2e3023c9447706d5a6cdda43662b296" width="1012" height="911" data-path="images/configuration/voicemaster/interface-permissions.gif" />
</Frame>

## Customizing your voice channel

The following commands can be done via the `#interface` channel.

### Renaming your voice channel

You can use the `voicemaster rename` command to change the name of your voice channel.

<Info>This command can only be used **once** every **10 minutes**.</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,voicemaster rename (name)
  ```

  ```javascript Example theme={null}
  ,voicemaster rename ethan's vc
  ```
</CodeGroup>

### Limiting the number of members

You can use the `voicemaster limit` command to set a limit on the number of members that can join your voice channel.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,voicemaster limit (number)
  ```

  ```javascript Example theme={null}
  ,voicemaster limit 5
  ```
</CodeGroup>

### Making your voice channel private

You can lock & hide your voice channel with the following commands.

* `voicemaster lock` - Prevents anyone from joining the voice channel.
  * `voicemaster unlock` - Allows anyone join the voice channel.
* `voicemaster ghost` - Hides the voice channel from the channel list.
  * `voicemaster unghost` - Reveals the voice channel in the channel list.

<Card title="Subscription Required" icon="medal" iconType="duotone" horizontal>
  You must have a [Tier 2 Subscription](/overview/donator-perks) to use the
  `voicemaster ghost` command.
</Card>

#### Permitting members to join

You can use the `voicemaster permit` command to allow specific members to join your voice channel.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,voicemaster permit (member or role)
  ```

  ```javascript Example theme={null}
  ,voicemaster permit @jonathan
  ```
</CodeGroup>

### Granting a role to members in your voice channel

You can use the `voicemaster role` command to set a role that members will receive when they join your voice channel.

<Info>You must have the `Manage Roles` permission to use this command.</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,voicemaster role (role)
  ```

  ```javascript Example theme={null}
  ,voicemaster role @Listening Party
  ```
</CodeGroup>

## Related commands

<AccordionGroup>
  <Accordion title="Claiming ownership">
    If the owner of a voice channel leaves, you can use the `voicemaster claim` command to take ownership of the voice channel.
  </Accordion>

  <Accordion title="Transferring ownership">
    You can use the `voicemaster transfer` command to transfer ownership of a voice channel to another member.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,voicemaster transfer (member)
      ```

      ```javascript Example theme={null}
      ,voicemaster transfer @jonathan
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Setting the channel as a music channel">
    You can use the `voicemaster music` command which will prevent members from speaking in the voice channel.
  </Accordion>
</AccordionGroup>