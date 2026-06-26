> For the complete documentation index, see [llms.txt](https://docs.bleh.rest/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.rest/security/moderation.md).

# Moderation

## Overview <a href="#overview" id="overview"></a>

Moderation commands require some basic setup before they can be used. This includes **moderation logs**, **mute roles**, and the **jailed role & channel**.




#### Creating the case logs & jail role

*Jail is a feature similar to mute, but it restricts users from all channels except `#jail`*

Use the `;setjail` command to create the case logs channel and jail role.




#### Creating the necessary mute roles

*This will create a **image mute**, and **reaction mute** role.*

Use the `;setmute` command to create the necessary mute roles.



Upon completion of the setup, you’ll notice a few new roles and channels in your server.

* **Image Muted** - Used to restrict users from uploading attachments.
* **Reaction Muted** - Used to restrict users from reacting to messages.
* **Jailed** - Used to restrict users from all channels except the `#jail` channel.
  * The jailed role can be renamed since it’s found by its id.

## Invoke Messages <a href="#invoke-messages" id="invoke-messages"></a>

You can customize the response for moderation commands and the direct message which will be sent after punishing the user.

The following moderation commands can be customized:

* `jail`, `kick`, `ban` & `mute`



Command response:

```
;invoke message (command) add [code]
;invoke message (command) add Kicked, {member.mention}
```

Direct messages:

```
;invoke dm (command) add [code]
;invoke dm (command) add Kicked, {member.mention}
```


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.bleh.rest/security/moderation.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.