> For the complete documentation index, see [llms.txt](https://docs.bleh.rest/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.rest/server/level.md).

# Level Rewards

## Getting started

Before you run any commands, it’s important to use the `levels enable` command otherwise XP will not be tracked for users. You can also use the `levels disable` command reset it.

## Ignoring channels, roles & members <a href="#ignoring-channels-and-roles" id="ignoring-channels-and-roles"></a>

You should immediately ignore channels, roles & member that you don’t want gaining XP. You can do this by using the `levels ignore` command.



```
Syntax: ;level ignore add [target]
Example: ;level ignore add #general

Syntax: ;level ignore remove [target]
Example: ;level ignore remove #general
```



## Setting up roles to reward

You can reward your members with roles when they reach a certain level. You can use the `level rewards add` command to add a level reward.





```
Syntax: ;level rewards add [level] [role]
Example: ;level rewards add 15 gang

Syntax: ;level rewards remove [role]
Example: ;level rewards remove gang
```



### Stacking reward roles <a href="#stacking-reward-roles" id="stacking-reward-roles"></a>

Stacking roles means that users will keep all the roles they’ve earned when they reach a new level, instead of only having the role for their current level. By default, this feature is enabled.

```
Syntax: ;level rewards stack [option]
Example: ;level rewards stack on
```

## Customizing level-up messages

You can customize the level-up message that will be sent when a user achieves a new level.



```
Syntax: ;level message [message]
Example: ;level message Good job, {user}! You leveled up to **Level {level}**
```

### Setting where the message is sent

You can set the channel where the level-up message will be sent. By default, the message is sent in the same channel where the user achieved the level.

```
Syntax: ;level channel [channel]
Example: ;level channel #levels
```



## Changing a member’s level <a href="#changing-a-members-level" id="changing-a-members-level"></a>

You can change a member’s level to a specific level.

```
Syntax: ;level set [member] [level]
Example: ;level set bender.py 15
```

## Changing the XP multiplier

You can change the XP multiplier to increase or decrease the amount of XP members receive.

<pre><code><strong>Syntax: ;level multiplier [multiplier]
</strong>Example: ;level multiplier 2

Syntax: ;level booster [multiplier]
Example: ;level booster 2

Syntax: ;level rolemultiplier add/remove [role] [multiplier]
Example: ;level rolemultiplier addVanity 3
</code></pre>

## Related commands <a href="#related-commands" id="related-commands"></a>

<details>

<summary>Viewing a user's level and XP</summary>

Use the `rank` command to view a user’s level and XP.

</details>

<details>

<summary>Viewing the XP leaderboard</summary>

Use the `level leaderboard` subcommand to highest XP earners in the server.

</details>

<details>

<summary>Viewing the level rewards</summary>

Use the `level rewards list` subcommand to view all level rewards.

</details>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.bleh.rest/server/level.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.