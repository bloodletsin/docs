> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Button Roles

> Allow your members to assign themselves roles by clicking a button.

## What are button roles?

Button roles are roles that are assigned to members when they click a button on an existing message or embed. They can be useful for letting members choose unique roles or as a way to verify themselves.

## Creating a button role

You can create multiple button roles for a single message.

<Warning>
  Button roles can only be placed on messages & embeds sent by bleh. Learn how to create an embed [**here**](/resources/scripting/embeds)!
</Warning>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,buttonrole add (message link) (role) (style) (emoji) (label)

  // Available styles: "green," "blurple," "gray," or "red."
  ```

  ```javascript Example theme={null}
  ,buttonrole add .../channels/... Verified green ✅ Verify
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/roles/button/add.gif?s=3636b8310f2de2dd6e1e01c8d30c673c" width="800" height="452" data-path="images/configuration/roles/button/add.gif" />
</Frame>

## Removing a button role

You can remove a specific button role by using the `buttonrole remove` command.

<Tip>
  You can use the `buttonrole list` command to see all button roles in your server.

  <Frame>
    <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/roles/button/list.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=1a4c43fd23bdede43d24f17231ade3f6" width="923" height="376" data-path="images/configuration/roles/button/list.png" />
  </Frame>
</Tip>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,buttonrole remove (message link) (button number)
  ```

  ```javascript Example theme={null}
  ,buttonrole remove .../channels/... 1
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/roles/button/remove.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=2db1ee7e6ea3c6209b982507a073852a" width="966" height="275" data-path="images/configuration/roles/button/remove.png" />
</Frame>

### Removing all button roles for a message

Additionally, you can remove all button roles from a message by using the `buttonrole removeall` command.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,buttonrole removeall (message link)
  ```

  ```javascript Example theme={null}
  ,buttonrole removeall .../channels/...
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/roles/button/removeall.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=e2b434c27a05f051da32228371c69ebe" width="985" height="245" data-path="images/configuration/roles/button/removeall.png" />
</Frame>

### Removing all button roles from the server

You can remove all button roles from the server by using the `buttonrole reset` command.

<Warning>
  Please note that this **cannot** be undone & will **permanently** remove **all** button roles from the
  server.
</Warning>

```
,buttonrole reset
```

<Frame>
  <img src="https://mintcdn.com/bleh/NOU9kBuI7_CopQLy/images/configuration/roles/button/reset.png?fit=max&auto=format&n=NOU9kBuI7_CopQLy&q=85&s=a4f66c55a7293802be840206cdc2b348" width="921" height="252" data-path="images/configuration/roles/button/reset.png" />
</Frame>