> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/miscellaneous/music.md).

# Music

## Configuration <a href="#configuration" id="configuration"></a>

### Set teh DJ role

You can set a DJ role which restricts who can control the music player.

```
Syntax: ;dj [role]
Example: ;dj DJ
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_NmfRmBjruH.png" alt=""><figcaption></figcaption></figure>

### Remove the DJ role

```
Syntax: ;dj [role]
Example: ;dj none
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_Nizp8f83XY.png" alt=""><figcaption></figcaption></figure>

## Queueing Music <a href="#queueing-music" id="queueing-music"></a>

You can queue music with the `play` command.

{% hint style="info" %}
By default, the `play` command will search **YouTube**. You’re able to provide a **URL** which will queue the music directly from the source you provide.
{% endhint %}

```
Syntax: ;play [query]
Example: ;play yeat, king tonka
```

## Managing the Queue

### Viewing the tracks in the queue <a href="#viewing-the-tracks-in-the-queue" id="viewing-the-tracks-in-the-queue"></a>

Use the `queue` command to view the tracks in the queue. Each track has a corresponding position which can be used to interact with the queue.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_McACRCO4Ce.png" alt=""><figcaption></figcaption></figure>

### Removing a track from the queue <a href="#removing-a-track-from-the-queue" id="removing-a-track-from-the-queue"></a>

Use the `queue remove` command to remove a track from the queue. You must provide the [track position](#viewing-the-tracks-in-the-queue) which can be found with the `queue` command.

```
Syntax: ;queue remove [position]
Example: ;queue remove 1
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_He8pvRpjBu.png" alt=""><figcaption></figcaption></figure>

## Controlling Playback

You can control playback with the following commands

<details>

<summary>Skipping to the next track</summary>

Use the `skip` command to skip to the next track.

</details>

<details>

<summary>Pausing &#x26; Resuming playback</summary>

Use the `pause` & `resume` commands to pause and resume playback.

</details>

<details>

<summary>Changing the track volume</summary>

Use the `volume` command to change the volume.

```
Syntax: ;volume [volume]
Example: ;volume 75
```

</details>

<details>

<summary>Setting the repeat mode</summary>

Use the `repeat` command to set the repeat mode.

```
Syntax: ;repeat [mode]
Example: ;repeat current
```

</details>

## Music Sources

* **Spotify**
* **SoundCloud**
* **YouTube**


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/miscellaneous/music.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
