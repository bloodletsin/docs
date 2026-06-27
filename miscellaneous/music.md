> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Music

> Listen to music from a variety of sources inside voice channels.

## Configuration

### Setting the DJ role

You can set a DJ role which restricts who can control the music player.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,settings dj (role)
  ```

  ```javascript Example theme={null}
  ,settings dj @DJ
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/miscellaneous/music/bind-dj.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=14e8c09fe03d8161543686c21b512a64" width="402" height="165" data-path="images/miscellaneous/music/bind-dj.png" />
</Frame>

### Auto play similar tracks

You can toggle auto play which will automatically play similar tracks when the queue is empty.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,settings autoplay (on or off)
  ```

  ```javascript Example theme={null}
  ,settings autoplay on
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/miscellaneous/music/bind-autoplay.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=98a2ba16495d260a512de82e5157bc7d" width="422" height="173" data-path="images/miscellaneous/music/bind-autoplay.png" />
</Frame>

## Queueing Music

You can queue music with the `play` command.

<Tip>
  By default, the `play` command will search **Deezer**. You're able to provide
  a **URL** which will queue the music directly from the source you provide.
</Tip>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,play (query or URL)
  ```

  ```javascript Example theme={null}
  ,play jeans 2hollis
  ,play https://open.spotify.com/track/6C2nVSSeXNqfoY8t6tliZ4
  ```
</CodeGroup>

## Managing the Queue

### Viewing the tracks in the queue

Use the `queue` command to view the tracks in the queue.
Each track has a corresponding position which can be used to interact with the queue.

<Frame>
  <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/miscellaneous/music/queue.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=c525eb4f58c1497b89b6920674b37c55" width="344" height="235" data-path="images/miscellaneous/music/queue.png" />
</Frame>

### Removing a track from the queue

Use the `queue remove` command to remove a track from the queue.
You must provide the [track position](#viewing-the-tracks-in-the-queue) which can be found with the `queue` command.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,queue remove (position)
  ```

  ```javascript Example theme={null}
  ,queue remove 2
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/miscellaneous/music/queue-remove.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=d4d4f7e5abf64a81111e1ba98bbbc7c0" width="393" height="175" data-path="images/miscellaneous/music/queue-remove.png" />
</Frame>

### Moving a track in the queue

Use the `queue move` command to move a track in the queue.
You must provide the [current position](#viewing-the-tracks-in-the-queue) and the new position.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,queue move (position) (new_position)
  ```

  ```javascript Example theme={null}
  ,queue move 3 1
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/miscellaneous/music/queue-move.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=79923c9850462d16b0fcd736b03f62eb" width="404" height="169" data-path="images/miscellaneous/music/queue-move.png" />
</Frame>

## Controlling Playback

You can control playback with the following commands

<AccordionGroup>
  <Accordion title="Skipping to the next track">
    Use the `skip` command to skip to the next track.
  </Accordion>

  <Accordion title="Pausing & Resuming playback">
    Use the `pause` & `resume` commands to pause and resume playback.
  </Accordion>

  <Accordion title="Seeking to a specific position">
    Use the `seek` command to seek to a specific position in the track.

    <Tip>
      The position must use the format `mm:ss`, (e.g. `1:20`).
    </Tip>

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,seek (position)
      ```

      ```javascript Example theme={null}
      ,seek 2:30
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Changing the track volume">
    Use the `volume` command to change the volume.

    <Tip>
      The percentage must be between `0` and `100`.
    </Tip>

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,volume (percentage)
      ```

      ```javascript Example theme={null}
      ;volume 50
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Setting the repeat mode">
    Use the `repeat` command to set the repeat mode.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,repeat (off | queue | current)
      ```

      ```javascript Example theme={null}
      ,repeat current
      ```
    </CodeGroup>
  </Accordion>
</AccordionGroup>

## Music Filters

You can use an equalizer preset to adjust how the audio sounds.

<Info>
  You can view which presets are applied with the `preset active` command.
</Info>

| Command            | Description                                                                 |
| ------------------ | --------------------------------------------------------------------------- |
| `preset soft`      | Cuts high and mid frequencies, allowing only low frequencies                |
| `preset 8d`        | Creates a stereo-like panning effect, rotating audio for immersive sound    |
| `preset chipmunk`  | Accelerates track playback to produce a high-pitched, chipmunk-like sound   |
| `preset boost`     | Enhances track with heightened bass and highs for a lively, energetic feel  |
| `preset vaporwave` | Slows track playback for nostalgic and vintage half-speed effect            |
| `preset vibrato`   | Introduces a wavering pitch effect for dynamic tone                         |
| `preset piano`     | Enhances mid and high tones for standout piano-based tracks                 |
| `preset metal`     | Amplifies midrange for a fuller, concert-like sound, ideal for metal tracks |
| `preset flat`      | Represents a neutral EQ setting with default levels across the board        |
| `preset karaoke`   | Filters out vocals from the track, leaving only the instrumental            |
| `preset nightcore` | Accelerates track playback for nightcore-style music                        |

## Music Sources

* **Deezer**
* **Spotify**
* **SoundCloud**
* **Apple Music**