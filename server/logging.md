> For the complete documentation index, see [llms.txt](https://docs.bleh.rest/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.rest/server/logging.md).

# Logging

## Overview

Logging allows you to log events in your server. This can be useful for keeping track of what’s happening in your server.

## Adding a logging event <a href="#adding-a-logging-event" id="adding-a-logging-event"></a>

You can add a logging event using the `logs add` command.



```
Syntax: ;logs add [event] [channel]
Example: ;logs add messages #server
```





## Removing a logging event

You can remove a logging event using the `logs remove` command.

```
Syntax: ;logs remove [event]
Example: ;logs remove messages 
```



## Ignoring a member or channel <a href="#ignoring-a-member-or-channel" id="ignoring-a-member-or-channel"></a>

You can ignore and unignore a member or channel from being logged using the `log ignore add` command.

```
Syntax: ;level ignore add [target]
Example: ;level ignore add #general

Syntax: ;level ignore remove [target]
Example: ;level ignore remove #general
```



## View all enabled logging events

You can use the `logs list` command to view all enabled logging events.
