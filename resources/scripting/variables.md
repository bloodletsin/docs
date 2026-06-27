> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/resources/scripting/variables.md).

# Variables

These variables are accessible throughout evelina and can be used in any command context which contains a `message` or `embed code` parameter (e.g. `welcome`, `leave` & `goodbye`)

## User Related Variables <a href="#user-related-variables" id="user-related-variables"></a>

| Variable             | Output                            |
| -------------------- | --------------------------------- |
| {user.id}            | Only users id                     |
| {user.name}          | Only users name                   |
| {user.nick}          | Only users nickname               |
| {user.display}       | Only users display name           |
| {user.mention}       | Mentions the user                 |
| {user.discriminator} | Only users discriminator          |
| {user.avatar}        | Only users avatar                 |
| {user.guild.avatar}  | Only users guild avatar           |
| {user.joined\_at}    | Joined date in timestamp format   |
| {user.created\_at}   | Creation date in timestamp format |

## Guild Related Variables <a href="#guild-related-variables" id="guild-related-variables"></a>

| Variable                      | Output                                      |
| ----------------------------- | ------------------------------------------- |
| {guild.id}                    | Only guild id                               |
| {guild.name}                  | Only guild name                             |
| {guild.icon}                  | Only guild icon                             |
| {guild.created\_at}           | Creation date in timestamp format           |
| {guild.count}                 | Only member count                           |
| {guild.count.format}          | Only guild count in ordinal format          |
| {guild.boost\_count}          | Only guild boost amount                     |
| {guild.boost\_count.format}   | Only guild boost amount in ordinal format   |
| {guild.booster\_count}        | Amount of people boosting                   |
| {guild.booster\_count.format} | Amount of people boosting in ordinal format |
| {guild.boost\_tier}           | Only guild's boost level                    |
| {guild.vanity}                | Only guild vanity                           |

## Lastfm Related Variables <a href="#guild-related-variables" id="guild-related-variables"></a>

{% tabs %}
{% tab title="Track" %}

| Variable            | Output                                  |
| ------------------- | --------------------------------------- |
| {track.name}        | Shows track name                        |
| {lower(track.name)} | Shows track name in lowercase           |
| {track.url}         | Shows the track lastfm url              |
| {track.image}       | Shows the track image                   |
| {track.plays}       | Shows the track’s plays on your account |
| {% endtab %}        |                                         |

{% tab title="Artist" %}

| Variable             | Output                                 |
| -------------------- | -------------------------------------- |
| {artist.name}        | Shows the artist name                  |
| {lower(artist.name)} | Shows artist name in lowercase         |
| {artist.url}         | Shows the artist lastfm url            |
| {artist.plays}       | Shows the artist plays on your account |
| {% endtab %}         |                                        |

{% tab title="Album" %}

| Variable            | Output                                |
| ------------------- | ------------------------------------- |
| {album.name}        | Shows the album name                  |
| {lower(album.name)} | Shows album name in lowercase         |
| {album.url}         | Shows the album lastfm url            |
| {album.plays}       | Shows the album plays on your account |
| {% endtab %}        |                                       |

{% tab title="User" %}

| Variable       | Output                                                |
| -------------- | ----------------------------------------------------- |
| {username}     | Shows your lastfm username                            |
| {useravatar}   | Shows your lastfm avatar                              |
| {scrobbles}    | Shows total number of songs scrobbled on your account |
| {lastfm.color} | Shows main color of lastfm logo                       |
| {lastfm.emoji} | Shows lastfm logo emoji                               |
| {% endtab %}   |                                                       |
| {% endtabs %}  |                                                       |

## Levels Related Variables

| Variable     | Output                                      |
| ------------ | ------------------------------------------- |
| {level}      | Shows level you reached to                  |
| {target\_xp} | Show new target xp amount you have to reach |

## Invite Tracker Related Variables

| Variable                 | Output                                    |
| ------------------------ | ----------------------------------------- |
| {inviter.id}             | Only inviter id                           |
| {inviter.name}           | Only inviter name                         |
| {inviter.display}        | Only inviter display name                 |
| {inviter.mention}        | Mentions the inviter                      |
| {inviter.avatar}         | Only inviters avatar                      |
| {inviter.regular\_count} | Number of regular invites the inviter has |
| {inviter.left\_count}    | Number of left invites the inviter has    |
| {inviter.fake\_count}    | Number of fake invites the inviter has    |
| {inviter.bonus\_count}   | Number of bonus invites the inviter has   |
| {inviter.total\_count}   | Total number of invites the inviter has   |

## Ticket Related Variables

| Variable       | Output                   |
| -------------- | ------------------------ |
| {user.id}      | Only ticket user id      |
| {user.name}    | Only ticket user name    |
| {support.role} | All ticket support roles |
| {topic}        | Name of the ticket topic |

## Punishments Related Variables

{% hint style="info" %}
Only available for `ban`, `unban`, `kick`, `mute`, `unmute`, `jail`, `unjail`
{% endhint %}

| Variable               | Output                                     |
| ---------------------- | ------------------------------------------ |
| {member.id}            | Shows id of the punished member            |
| {member.name}          | Shows name of the punished member          |
| {member.mention}       | Shows mention the punished member          |
| {member.discriminator} | Shows discriminator of the punished member |
| {member.avatar}        | Shows avatar of the punished member        |
| {reason}               | Shows reason of the punishment             |
| {duration}             | Shows duration for mute/jail               |
| {appeal.url}           | Show appeal url of the punishment          |
| {case.id}              | Show case id of the punishment             |


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/resources/scripting/variables.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
