> For the complete documentation index, see [llms.txt](https://docs.bleh.rest/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.rest/miscellaneous/tickets.md).

# Tickets

## Ticket Setup

### Support Role

Define a support role for the ticket system. This role can close tickets, view them and add/remove members from the ticket.

```
Syntax: ;ticket support add [topic] [role]
Example: ;ticket support add default Staff
```



### Category

Set a category in which Bleh should create all new tickets.

```
Syntax: ;ticket settings category [topic] [category]
Example: ;ticket settings category [topic] #tickets
```





### Transcripts

Set a channel in which all transcripts of closed tickets should be sent.

```
Syntax: ;ticket settings logs [channel]
Example: ;ticket settings logs #transcripts
```



## Ticket Topics

Create multiple ticket topics to have a better overview of your tickets.

```
Syntax: ;ticket topics
Example: ;ticket topics
```

After you have executed the command, you will receive a message with two buttons with which you can create or delete topics (categories).



To add your topic, click on "add topic" and fill out the modal.



To avoid problems with emoji processing, we recommend using the command `;emoji info [emoji]` to find out the **Markdown** and copy it 1:1 for the ticket system.



You can also edit existing topics or create them manually.

```
;ticket topic add [name]
;ticket topic remove [name]

;ticket topic name [old] [new]
;ticket topic description [name] [description]
;ticket topic emoji [name] [emoji]
```





## Ticket Embed

To create a ticket you also need the ticket embed.

```
Syntax: ;ticket send [channel]
Example: ;ticket send #ticket
```



If you don't want the standard ticket embed, you can create one yourself. Go to <https://bleh.rest/embed>.



After you have finished designing your embed, click on "Generate Embed Code" and copy it with "Copy Embed Code"

```
Syntax: ;ticket send [channel] [code]
Example: ;ticket send #ticket {embed}$v{description: Create a Ticket}
```



## Ticket Open Embed

Change the message sent when a new ticket is created.

<pre><code><strong>Syntax: ;ticket settings embed [topic] [code]
</strong>Example: ;ticket settings embed default {embed}$v{description: Support will be with you shortly}
</code></pre>





## Ticket Modals

Now you can add a modal that opens before a ticket is opened to have questions answered.

```
Syntax: ;ticket modal add [topic] [name] [description]
Example: ;ticket modal add Support Question What is your Question?
```





To display in the ticket message what the user has entered in the modal, you have to take the code and insert {code} into your open embed message like this



````
Syntax: ;ticket settings embed [topic] [code]
Example: ;ticket settings embed Support {embed}$v{content: {user.mention} | {support.role}}$v{description: ## :support: Support}$v{color: #729bb0}$v{author: name: {user.name} ({user.id}) && icon: {user.avatar}}$v{field: name: > Question && value: ```{lNp6A5kA}```}
````



Here is an example of what it would look like if a user wants to open a ticket:



Here is an example of what it would look like if a user opened a support ticket and filled out the modal:



## Ticket Channel Names

If you want you can change the default ticket channel name with these commands.

```
Syntax: ;ticket topic channelname [name] [channelname]
Example: ;ticket topic channelname Support 💰-{user.name}
```



To remove a channelname from a topic you can do it with this command. Just leave the \[channelname] variable empty.

```
Syntax: ;ticket topic channelname [name]
Example: ;ticket topic channelname Support
```



## Ticket Channel Topic

If you want you can change the default ticket channel topic with these commands.

```
Syntax: ;ticket topic channeltopic [name] [channeltopic]
Example: ;ticket topic channeltopic Support 💰-{user.name}
```



To remove a channeltopic from a topic you can do it with this command. Just leave the \[channeltopic] variable empty.

```
Syntax: ;ticket topic channeltopic [name]
Example: ;ticket topic channeltopic Support
```




---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.bleh.rest/miscellaneous/tickets.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.