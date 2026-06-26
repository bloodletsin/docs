> For the complete documentation index, see [llms.txt](https://docs.bleh.rest/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.rest/security/antinuke.md).

# Antinuke

## Information



Antinuke is triggered by a threshold set **per user**.

Your antinuke should **never** have to be higher than 5. Antinuke will not work as well if it's threshold is set high. We recommend a threshold between 1 and 5.

## Parameters

| Name       | Description                   |
| ---------- | ----------------------------- |
| threshold  | Threshold to trigger antinuke |
| punishment | Action to be taken on trigger |
| time       | Threshold for account age     |



## Punishments

Click the following to view all antinuke punishments available:


[Punishments](/resources/punishments.md)


## Admins & Whitelisted <a href="#admins-and-whitelisted" id="admins-and-whitelisted"></a>

You can whitelist members from triggering antinuke by using `antinuke whitelist [user]`.

You can also grant antinuke admin to a user, which allows them to modify antinuke settings. You can do this by using `[prefix] antinuke admin [user]`. Only give this to people you trust.



## Antinuke Logs <a href="#antinuke-logs" id="antinuke-logs"></a>

You can set a channel to send antinuke logs by using `antinuke logs`. Whenever antinuke is triggered, a message will be sent to that channel. It is recommended that you set this up.

## Antinuke Recommended Configuration

If you don't know how to configure your Antinuke, here is our recommended config for the Antinuke module.

```
// Role Config
antinuke rolecreate enable 3 strip
antinuke roledelete enable 1 strip
antinuke editrole enable ban
antinuke giverole enable strip

// Channel Config
antinuke channelcreate enable 3 strip
antinuke channeldelete enable 1 strip

// Role Moderation
antinuke kick enable 3 kick
antinuke ban enable 3 kick
antinuke botadd enable strip
```
