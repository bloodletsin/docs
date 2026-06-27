> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/miscellaneous/counters.md).

# Counters

Counters are a way to keep track of different statistics in your server. You can track things humans only, bots, and more.

## Creating a Counter <a href="#creating-a-counter" id="creating-a-counter"></a>

To create a counter, run the following command:

```
Syntax: ;counter add [counter_type] [channel_type] [name]
Example: ;counter add humans category {target} humans
```

Output:

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202024-07-11%20160802.png" alt=""><figcaption></figcaption></figure>

### Break it Down <a href="#break-it-down" id="break-it-down"></a>

Firstly, you need to replace `[counter_type]` with an accepted counter type. You can find a list of those here: [Accepted Counter Types](#accepted-counter-types)

Next, you need to replace `[channel_type]` with an accepted channel type. You can find a list of those here: [Accepted Channel Types](#accepted-channel-types)

Lastly, you need to specify a name. The name can be anything. `{target}` indicates the number from the counter you set. In our example, we said humans. evelina would create a category named "587 humans". If I were to name it `ppl: {target}` instead, evelina would create a category named "ppl: 587".

## Remove a Counter <a href="#remove-a-counter" id="remove-a-counter"></a>

To remove a counter, run the following command:

```
Syntax: ;counter remove [counter_type]
Example: ;counter remove humans
```

This would remove the "humans" counter from the server. evelina will send an embed confirming the removal of the counter.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202024-07-11%20160818.png" alt=""><figcaption></figcaption></figure>

## Accepted Counter Types

| members  | All members from the server (including bots) |
| -------- | -------------------------------------------- |
| humans   | All members from the server (excluding bots) |
| bots     | All bots from the server                     |
| boosters | All server boosters                          |
| voice    | All members in a voice channel               |
| role     | All members in a certain role                |
| boosts   | All boosts from the server                   |

## Accepted Channel Types <a href="#accepted-channel-types" id="accepted-channel-types"></a>

| Type     | Description                            |
| -------- | -------------------------------------- |
| Voice    | Voice channel                          |
| Stage    | Stage channel (community servers only) |
| Text     | Text channel                           |
| Category | Channel category                       |


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/miscellaneous/counters.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
