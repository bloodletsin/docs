> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Spotify

> Control your Spotify account through Discord.

## Connecting your Spotify account

<Steps>
  <Step title="Start the Process">
    Use the `spotify login` command, and follow the link provided in the
    response.

    <Frame>
      <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/integrations/spotify/authentication.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=8ce337d79dde628a729c32ee547dad58" width="927" height="315" data-path="images/integrations/spotify/authentication.png" />
    </Frame>
  </Step>

  <Step title="Grant Access">
    After following the link, you will be asked to grant access to your
    **Spotify** account.

    <Frame>
      <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/integrations/spotify/authorization.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=cf70574ee48d01c0a0f8f48a18618b82" width="397" height="429" data-path="images/integrations/spotify/authorization.png" />
    </Frame>
  </Step>

  <Step title="Submit Code">
    Once you've granted access, you will be given a code to submit in Discord.

    <Frame>
      <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/integrations/spotify/input.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=3948c0f9d71127db435309de1056c791" width="489" height="307" data-path="images/integrations/spotify/input.png" />
    </Frame>
  </Step>
</Steps>

If you no longer wish to use the **Spotify integration**, you can use the `spotify logout` command to disconnect your account from bleh.

## Controlling your Spotify Playback

<Warning>
  You must be a **Spotify Premium** subscriber to control your playback with
  bleh.
</Warning>

### Playing a track

You can use the `spotify play` command to immediately start playing a track, or
if you'd like to queue a track for later, use the `spotify queue` command.

<Info>
  You can also mention a member to play the track they're currently listening
  to.
</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,spotify play (query or member)
  ```

  ```javascript Example theme={null}
  ,spotify play Lancey Foux LEFT RIGHT
  ,spotify play @jonathan
  ```
</CodeGroup>

### Adjusting the volume

You can use the `spotify volume` command to adjust the volume of the active
device.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,spotify volume (percentage)
  ```

  ```javascript Example theme={null}
  ,spotify volume 50
  ```
</CodeGroup>

### Seeking to a specific position

You can use the `spotify seek` command to seek to a specific position in the
current track.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,spotify seek (position)
  ```

  ```javascript Example theme={null}
  ,spotify seek 1:30
  ```
</CodeGroup>

### Changing the playback device

You can use the `spotify device` command to change the device that **Spotify** is
playing on.

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/integrations/spotify/device.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=96293b8528081777cef2e182085e5f3e" width="546" height="187" data-path="images/integrations/spotify/device.png" />
</Frame>

### Interacting with the queue

The following commands can be used to interact with the queue

| Command            | Description                         |
| ------------------ | ----------------------------------- |
| `spotify next`     | Skip to the next track in the queue |
| `spotify previous` | Play the previous track             |
| `spotify pause`    | Pause the current track             |
| `spotify resume`   | Resume the current track            |
| `spotify shuffle`  | Toggle queue shuffling              |
| `spotify repeat`   | Toggle repeating the track or queue |

## Non-Premium Commands

The following commands can be used without a **Spotify Premium** subscription

<AccordionGroup>
  <Accordion title="Liking the current track">
    You can use the `spotify like` command to like the current track.

    <Tip>
      You can also use the `spotify unlike` command to remove the like.
    </Tip>
  </Accordion>

  <Accordion title="Viewing your top artists and tracks">
    You can use the `spotify artists` and `spotify tracks` commands to
    view your top artists and tracks for a specified time frame.

    <Info>
      The timeframe must be `1m`, `6m`, or `1y`.
    </Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,spotify artists (timeframe)
      ,spotify tracks (timeframe)
      ```

      ```javascript Example theme={null}
      ,spotify artists 1m
      ,spotify tracks 6m
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Playing your current track in a voice channel">
    You can use the `spotify vc` command to play your current track in a
    voice channel.
  </Accordion>
</AccordionGroup>