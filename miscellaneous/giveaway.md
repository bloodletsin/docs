> For the complete documentation index, see [llms.txt](https://docs.bleh.rest/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.rest/miscellaneous/giveaway.md).

# Giveaway

## Starting a Giveaway

You can start a giveaway with the `giveaway create` command.

```
Syntax: ;giveaway create [channel] [time] [winners] [prize]
Example: ;giveaway create #giveaway 12h 1 Nitro
```





## Giveaway Requirements <a href="#changing-the-details" id="changing-the-details"></a>

You can set a `role`, `messages`, `level` & `invites` as requirement to join a giveaway.

```
Syntax: ;giveaway create [channel] [time] [winners] [prize]
Example: ;giveaway create #giveaway 12h 1 Nitro --role @Trusted --messages 100 --level 10
```





## Giveaway Bonus Entries <a href="#changing-the-details" id="changing-the-details"></a>

You can set a `role` that get double entries for your giveaway.

```
Syntax: ;giveaway create [channel] [time] [winners] [prize]
Example: ;giveaway create #giveaway 12h 1 Nitro --bonus @Booster
```





## Giveaway Blacklist <a href="#changing-the-details" id="changing-the-details"></a>

You can set a `role` that can't join your giveaway.

```
Syntax: ;giveaway create [channel] [time] [winners] [prize]
Example: ;giveaway create #giveaway 12h 1 Nitro --ignore @Jail
```





## Changing the details <a href="#changing-the-details" id="changing-the-details"></a>

You can customize the giveaway with the following commands

<details>

<summary>Changing the host</summary>

Use the `giveaway edit host` command to change the giveaway host.

```
Syntax: ;giveaway edit host [message] [host]
Example: ;giveaway edit host 1256932539411468380 bender.py
```

</details>

<details>

<summary>Changing the prize</summary>

Use the `giveaway edit prize` command to change the giveaway prize.

```
Syntax: ;giveaway edit price [message] [price]
Example: ;giveaway edit price 1256932539411468380 Nitro Yearly
```

</details>

<details>

<summary>Changing the duration</summary>

Use the `giveaway edit duration` command to change the duration of the giveaway.

```
Syntax: ;giveaway edit duration [message] [duration]
Example: ;giveaway edit duration 1256932539411468380 1d
```

</details>

<details>

<summary>Changing the amount of winners</summary>

Use the `giveaway edit winners` command to change the amount of people that can win the giveaway.

```
Syntax: ;giveaway edit winners [message] [winners]
Example: ;giveaway edit winners 1256932539411468380 2
```

</details>

<details>

<summary>Changing the requirements</summary>

Use the `giveaway requirements` command to requirements for a giveaway.

```
Syntax: ;giveaway requirements add/remove/edit [message] [flag] [input]
Example: ;giveaway requirements edit role 1256932539411468380 Moderator
```

</details>

## Ending a Giveaway

You can end a giveaway early with the `giveaway end` command.

```
Syntax: ;giveaway end [message]
Example: ;giveaway end 1256932539411468380
```



## Rerolling a Giveaway <a href="#rerolling-a-giveaway" id="rerolling-a-giveaway"></a>

You can reroll the winners of a giveaway with the `giveaway reroll` command.

```
Syntax: ;giveaway reroll [message] [winners]
Example: ;giveaway reroll 1256932539411468380 1
```



## Viewing all Giveaways

You can view all giveaways with the `giveaway list` command.
