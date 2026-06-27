> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/economy/general.md).

# General

## How can I earn money?

You can earn money by using these commands:

* beg
* bonus
* work
* slut
* daily

You can also rob other users to get money or vote on top.gg for evelina to get money.

## What are the basic commands that I need?

With `deposit` you can deposit money into your bank account so you can't get robbed or transfer money to other users.

```
Syntax: ,deposit [amount]
Example: ,deposit 125
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-26%20024510.png" alt=""><figcaption></figcaption></figure>

With `withdraw` you can withdraw your money to gamble with it or buy things with it.

```
Syntax: ,withdraw [amount]
Example: ,withdraw 125
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-26%20024705.png" alt=""><figcaption></figcaption></figure>

With `transfer` you can give money to your friends, but keep in mind there is a daily limit of 10 Million coins.

```
Syntax: ;transfer [member] [amount]
Example: ;transfer bender.py 125
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Screenshot%202025-03-26%20025029.png" alt="" width="359"><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/economy/general.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
