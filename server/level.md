> For the complete documentation index, see [llms.txt](https://docs.bleh.rest/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.rest/server/level.md).

# Level Rewards

## Getting started

Before you run any commands, it’s important to use the `levels enable` command otherwise XP will not be tracked for users. You can also use the `levels disable` command reset it.

## Ignoring channels, roles & members 

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



### Stacking reward roles 

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



## Changing a member’s level 

You can change a member’s level to a specific level.

```
Syntax: ;level set [member] [level]
Example: ;level set bender.py 15
```

## Changing the XP multiplier

You can change the XP multiplier to increase or decrease the amount of XP members receive.

```
**Syntax: ;level multiplier [multiplier]
**Example: ;level multiplier 2

Syntax: ;level booster [multiplier]
Example: ;level booster 2

Syntax: ;level rolemultiplier add/remove [role] [multiplier]
Example: ;level rolemultiplier addVanity 3

```

## Related commands 



Viewing a user's level and XP

Use the `rank` command to view a user’s level and XP.





Viewing the XP leaderboard

Use the `level leaderboard` subcommand to highest XP earners in the server.





Viewing the level rewards

Use the `level rewards list` subcommand to view all level rewards.
