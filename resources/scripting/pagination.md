> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/resources/scripting/pagination.md).

# Pagination

## Setup

{% stepper %}
{% step %}

#### Create the embed

Firstly you must create the embed to work with pagination. `;``paginate create [embed]`

<img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_3gN9ww9LpK.png" alt="" data-size="original">
{% endstep %}

{% step %}

#### Add the next page

You can now add further pages to your embed. This command works with adding any number of pages required. `;paginate add [message] [embed]`

<img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_mbBKE5leXJ%20(1).png" alt="" data-size="original">
{% endstep %}

{% step %}

#### Edit a paginated embed

If you need to edit a page you’ve made during setup, you can use the command below. `;paginate edit [message] [page] [embed]`

<img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_xbI9aXdD0M.png" alt="" data-size="original">
{% endstep %}

{% step %}

#### Removing a page

If you want to remove a page you have setup, you can use the below command `;paginate remove [message] [page]`

<img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_xgBDsOsbzp.png" alt="" data-size="original">
{% endstep %}
{% endstepper %}

## List all pagination messages

You can use the `paginate list` command to view all pagination messages.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_V6Tgyqz7H1.png" alt="" width="250"><figcaption></figcaption></figure>

## Clear all pages of a pagination message

You can use the `paginate clear` command to clear all pages of a pagination messages.

```
Syntax: ;paginate clear [message]
Example: ;paginate clear .../channels/...
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_IlvhDMtLya.png" alt="" width="402"><figcaption></figcaption></figure>

## Reset all pagination messages

You can use the `paginate reset` command to reset all pagination messages.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_xEuBdsqyKS.png" alt="" width="440"><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/resources/scripting/pagination.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
