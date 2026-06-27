> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/miscellaneous/giveaway.md).

# Giveaway

## Starting a Giveaway

You can start a giveaway with the `giveaway create` command.

```
Syntax: ;giveaway create [channel] [time] [winners] [prize]
Example: ;giveaway create #giveaway 12h 1 Nitro
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202024-12-21%20221201.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202024-12-21%20221228.png" alt=""><figcaption></figcaption></figure>

## Giveaway Requirements <a href="#changing-the-details" id="changing-the-details"></a>

You can set a `role`, `messages`, `level` & `invites` as requirement to join a giveaway.

```
Syntax: ;giveaway create [channel] [time] [winners] [prize]
Example: ;giveaway create #giveaway 12h 1 Nitro --role @Trusted --messages 100 --level 10
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202024-12-21%20223108.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202024-12-21%20223128.png" alt=""><figcaption></figcaption></figure>

## Giveaway Bonus Entries <a href="#changing-the-details" id="changing-the-details"></a>

You can set a `role` that get double entries for your giveaway.

```
Syntax: ;giveaway create [channel] [time] [winners] [prize]
Example: ;giveaway create #giveaway 12h 1 Nitro --bonus @Booster
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202024-12-25%20235555.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/imaefefge.png" alt=""><figcaption></figcaption></figure>

## Giveaway Blacklist <a href="#changing-the-details" id="changing-the-details"></a>

You can set a `role` that can't join your giveaway.

```
Syntax: ;giveaway create [channel] [time] [winners] [prize]
Example: ;giveaway create #giveaway 12h 1 Nitro --ignore @Jail
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-01-09%20052437.png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-01-09%20052454.png" alt=""><figcaption></figcaption></figure>

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

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_mnyT6DImRt.png" alt=""><figcaption></figcaption></figure>

## Rerolling a Giveaway <a href="#rerolling-a-giveaway" id="rerolling-a-giveaway"></a>

You can reroll the winners of a giveaway with the `giveaway reroll` command.

```
Syntax: ;giveaway reroll [message] [winners]
Example: ;giveaway reroll 1256932539411468380 1
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_tgGgMv4dan.png" alt=""><figcaption></figcaption></figure>

## Viewing all Giveaways

You can view all giveaways with the `giveaway list` command.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_pEZ7547S6X.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/miscellaneous/giveaway.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
