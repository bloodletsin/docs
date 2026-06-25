> For the complete documentation index, see [llms.txt](https://docs.bleh.rest/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.rest/server/voicemaster.md).

# VoiceMaster

## Getting started <a href="#getting-started" id="getting-started"></a>

The first step to using **VoiceMaster** is to use the `voicemaster setup` command.

{% hint style="info" %}
The created channels can be moved and renamed to your liking.
{% endhint %}

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Discord_m7JBotuepB.png" alt=""><figcaption></figcaption></figure>

### What is the interface channel?

The `#interface` channel will contain an embed with buttons that allow members to customize their temporary voice channel. This channel should be locked to keep the embed message at the top of the channel.

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Discord_7gcgOzc21R.png" alt="" width="396"><figcaption></figcaption></figure>

### What is the Join to Create channel? <a href="#what-is-the-join-to-create-channel" id="what-is-the-join-to-create-channel"></a>

The **Join to Create** channel is where members will join to create their temporary voice channel. This channel is required for the **VoiceMaster** system to work.

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/UnbenanntesVideoMitClipchamperstelltonline-video-cutter.com-ezgif.com-video-to-gif-converter.gif" alt="" width="360"><figcaption></figcaption></figure>

## Customizing new voice channels

You can customize what the temporary voice channels look like when they’re created.

<details>

<summary>Redirecting voice channels</summary>

Redirect voice channels to a specific category.

```
Syntax: ;voicemaster category [category]
Example: ;voicemaster category Voice Channels
```

</details>

<details>

<summary>Setting the default channel name</summary>

The name can use the `{user}`, `{user.name}` and `{user.display_name}` variables.

```
Syntax: ;voicemaster name [name]
Example: ;voicemaster name {user.display_name}'s vc
```

</details>

<details>

<summary>Setting the default channel bitrate</summary>

The bitrate must be between `8` and `384`.

```
Syntax: ;voicemaster bitrate [bitrate]
Example: ;voicemaster bitrate 384
```

</details>

<details>

<summary>Setting the default channel region</summary>

The region must be one of the following\
`brazil`, `hongkong`, `india`, `japan`, `rotterdam`, `russia`, `singapore`, `south-korea`, `southafrica`, `sydney`, `us-central`, `us-east`, `us-south`, `us-west`

```
Syntax: ;voicemaster region [region]
Example: ;voicemaster region russia
```

</details>

## Customizing your voice channel <a href="#customizing-your-voice-channel" id="customizing-your-voice-channel"></a>

The following commands can be done via the `#interface` channel.

### Renaming your voice channel <a href="#renaming-your-voice-channel" id="renaming-your-voice-channel"></a>

You can use the `voice rename` command to change the name of your voice channel.

{% hint style="info" %}
This command can only be used **once** every **10 minutes**.
{% endhint %}

```
Syntax: ;voice rename [name]
Example: ;voice rename Valorant Voice
```

### Limiting the number of members <a href="#limiting-the-number-of-members" id="limiting-the-number-of-members"></a>

You can use the `voice limit` command to set a limit on the number of members that can join your voice channel.

```
Syntax: ;voice limit [limit]
Example: ;voice limit 5
```

### Making your voice channel private <a href="#making-your-voice-channel-private" id="making-your-voice-channel-private"></a>

You can lock & hide your voice channel with the following commands.

* `voice lock` - Prevents anyone from joining the voice channel.
  * `voice unlock` - Allows anyone join the voice channel.
* `voice hide` - Hides the voice channel from the channel list.
  * `voice reveal` - Reveals the voice channel in the channel list.

### Permitting members to join

You can use the `voice permit` command to allow specific members to join your voice channel.

```
Syntax: ;voice permit [member]
Example: ;voice permit bender.py
```

## Related commands

<details>

<summary>Claiming ownership</summary>

If the owner of a voice channel leaves, you can use the `voice claim` command to take ownership of the voice channel.

</details>

<details>

<summary>Transferring ownership</summary>

You can use the `voice transfer` command to transfer ownership of a voice channel to another member.

```
Syntax: ;voice transfer [member]
Example: ;voice transfer bender.py
```

</details>

<details>

<summary>Change channel status</summary>

You can use the `voice status` command to change current channel status.

```
Syntax: ;voice status [status]
Example: ;voice status Gaming
```

</details>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.bleh.rest/server/voicemaster.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.