> For the complete documentation index, see [llms.txt](https://docs.bleh.rest/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.rest/server/bump.md).

# Bump Reminder

## Why use bump reminders?

Receiving reminders to bump your server on **DISBOARD** can help you increase your server’s visibility and attract new members. You can set up the **DISBOARD** bot by clicking [here](https://discord.com/oauth2/authorize?scope=identify+guilds+guilds.join\&response_type=code\&approval_prompt=auto\&client_id=302050872383242240\&redirect_uri=https%3A%2F%2Fdisboard.org%2Fsite%2Foauth-callback).

## Setting up bump reminders <a href="#setting-up-bump-reminders" id="setting-up-bump-reminders"></a>

Once you’ve invited the **DISBOARD** bot, you can set up bump reminders by setting the channel where you want to receive reminders to run `/bump` every **two hours**.

```
;bumpreminder enable
```



## Customizing bump reminders

### Changing the reminder message <a href="#changing-the-reminder-message" id="changing-the-reminder-message"></a>

You can change the reminder message with the `bumpreminder reminder` command. This is the message that will be sent every **two hours** when it’s time to `/bump` the server.



```
Syntax: ;bumpreminder reminder [code]
Example: ;bumpreminder reminder Bump the server using **/bump**
```



### Changing the thank you message <a href="#changing-the-thank-you-message" id="changing-the-thank-you-message"></a>

You can change the message which will be sent after bumping the server with the `bumpreminder thankyou` command.



```
Syntax: ;bumpreminder thankyou [code]
Example: ;bumpreminder thankyou Thanks, {user.mention}
```
