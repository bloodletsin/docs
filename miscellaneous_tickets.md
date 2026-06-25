> For the complete documentation index, see [llms.txt](https://docs.bleh.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.bot/miscellaneous/tickets.md).

# Tickets

## Ticket Setup

### Support Role

Define a support role for the ticket system. This role can close tickets, view them and add/remove members from the ticket.

```
Syntax: ;ticket support add [topic] [role]
Example: ;ticket support add default Staff
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202024-12-18%20185708.png" alt=""><figcaption></figcaption></figure>

### Category

Set a category in which Bleh should create all new tickets.

```
Syntax: ;ticket settings category [topic] [category]
Example: ;ticket settings category [topic] #tickets
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Discord_fl0HJxxUzr.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
If you do not use topics or do not want each topic to have its own category, use "default" to set the default category
{% endhint %}

### Transcripts

Set a channel in which all transcripts of closed tickets should be sent.

```
Syntax: ;ticket settings logs [channel]
Example: ;ticket settings logs #transcripts
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Discord_sbVwmyZwhJ.png" alt=""><figcaption></figcaption></figure>

## Ticket Topics

Create multiple ticket topics to have a better overview of your tickets.

```
Syntax: ;ticket topics
Example: ;ticket topics
```

After you have executed the command, you will receive a message with two buttons with which you can create or delete topics (categories).

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Bildschirmfoto%202024-08-03%20um%2016.19.55%20(1).png" alt="" width="302"><figcaption></figcaption></figure>

To add your topic, click on "add topic" and fill out the modal.

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Bildschirmfoto%202024-08-03%20um%2016.23.38.png" alt="" width="375"><figcaption></figcaption></figure>

To avoid problems with emoji processing, we recommend using the command `;emoji info [emoji]` to find out the **Markdown** and copy it 1:1 for the ticket system.

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Bildschirmfoto%202024-08-06%20um%2012.52.04.png" alt="" width="375"><figcaption></figcaption></figure>

You can also edit existing topics or create them manually.

```
;ticket topic add [name]
;ticket topic remove [name]

;ticket topic name [old] [new]
;ticket topic description [name] [description]
;ticket topic emoji [name] [emoji]
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Bildschirmfoto%202024-08-06%20um%2021.18.43-imageonline.co-merged.png" alt="" width="563"><figcaption></figcaption></figure>

{% hint style="warning" %}
It is important that if you create a category and want to use an emoji, the emoji must be on the same server as the bot.
{% endhint %}

## Ticket Embed

To create a ticket you also need the ticket embed.

```
Syntax: ;ticket send [channel]
Example: ;ticket send #ticket
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Bildschirmfoto%202024-08-03%20um%2016.27.57.png" alt="" width="375"><figcaption></figcaption></figure>

If you don't want the standard ticket embed, you can create one yourself. Go to <https://bleh.bot/embed>.

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Bildschirmfoto%202024-08-03%20um%2016.31.14.png" alt=""><figcaption></figcaption></figure>

After you have finished designing your embed, click on "Generate Embed Code" and copy it with "Copy Embed Code"

```
Syntax: ;ticket send [channel] [code]
Example: ;ticket send #ticket {embed}$v{description: Create a Ticket}
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Bildschirmfoto%202024-08-03%20um%2016.34.48.png" alt=""><figcaption></figcaption></figure>

## Ticket Open Embed

Change the message sent when a new ticket is created.

<pre><code><strong>Syntax: ;ticket settings embed [topic] [code]
</strong>Example: ;ticket settings embed default {embed}$v{description: Support will be with you shortly}
</code></pre>

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Discord_OSxPuieuZR.png" alt="" width="506"><figcaption></figcaption></figure>

{% hint style="warning" %}
If you do not use topics or do not want each topic to have its own category, use "default" to set the default category
{% endhint %}

## Ticket Modals

Now you can add a modal that opens before a ticket is opened to have questions answered.

```
Syntax: ;ticket modal add [topic] [name] [description]
Example: ;ticket modal add Support Question What is your Question?
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Bildschirmfoto%202024-09-09%20um%206.17.20 PM.png" alt="" width="563"><figcaption></figcaption></figure>

{% hint style="warning" %}
It is now important to save this code as you will need it to retrieve the user response.
{% endhint %}

To display in the ticket message what the user has entered in the modal, you have to take the code and insert {code} into your open embed message like this

{% embed url="<https://docs.bleh.bot/server/tickets#ticket-open-embed>" %}

````
Syntax: ;ticket settings embed [topic] [code]
Example: ;ticket settings embed Support {embed}$v{content: {user.mention} | {support.role}}$v{description: ## :support: Support}$v{color: #729bb0}$v{author: name: {user.name} ({user.id}) && icon: {user.avatar}}$v{field: name: > Question && value: ```{lNp6A5kA}```}
````

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202024-12-18%20185204.png" alt="" width="563"><figcaption></figcaption></figure>

Here is an example of what it would look like if a user wants to open a ticket:

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Bildschirmfoto%202024-09-09%20um%206.37.40 PM.png" alt="" width="375"><figcaption></figcaption></figure>

Here is an example of what it would look like if a user opened a support ticket and filled out the modal:

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Bildschirmfoto%202024-09-09%20um%206.33.37 PM.png" alt="" width="563"><figcaption></figcaption></figure>

## Ticket Channel Names

If you want you can change the default ticket channel name with these commands.

```
Syntax: ;ticket topic channelname [name] [channelname]
Example: ;ticket topic channelname Support 💰-{user.name}
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202024-12-30%20033548.png" alt=""><figcaption></figcaption></figure>

To remove a channelname from a topic you can do it with this command. Just leave the \[channelname] variable empty.

```
Syntax: ;ticket topic channelname [name]
Example: ;ticket topic channelname Support
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202024-12-30%20033717.png" alt=""><figcaption></figcaption></figure>

## Ticket Channel Topic

If you want you can change the default ticket channel topic with these commands.

```
Syntax: ;ticket topic channeltopic [name] [channeltopic]
Example: ;ticket topic channeltopic Support 💰-{user.name}
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202024-12-30%20034035.png" alt=""><figcaption></figcaption></figure>

To remove a channeltopic from a topic you can do it with this command. Just leave the \[channeltopic] variable empty.

```
Syntax: ;ticket topic channeltopic [name]
Example: ;ticket topic channeltopic Support
```

<figure><img src="https://github.com/BlehServices/docs/blob/main/.gitbook/assets/Screenshot%202024-12-30%20034205.png" alt=""><figcaption></figcaption></figure>


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.bleh.bot/miscellaneous/tickets.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.