> For the complete documentation index, see [llms.txt](https://docs.bleh.rest/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.rest/server/voicemaster.md).

# VoiceMaster

## Getting started <a href="#getting-started" id="getting-started"></a>

The first step to using **VoiceMaster** is to use the `voicemaster setup` command.





### What is the interface channel?

The `#interface` channel will contain an embed with buttons that allow members to customize their temporary voice channel. This channel should be locked to keep the embed message at the top of the channel.



### What is the Join to Create channel? <a href="#what-is-the-join-to-create-channel" id="what-is-the-join-to-create-channel"></a>

The **Join to Create** channel is where members will join to create their temporary voice channel. This channel is required for the **VoiceMaster** system to work.



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
