> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Fake Permissions

> Restrict moderators to only use bleh for moderation.

### Why use fake permissions?

Fake permissions negate the possibility of a rogue moderator using a script which floods the **Discord API** and mass bans all members, or any other harmful action.
It's a security measure which ensures that your server can't be nuked whatsoever.

### How do fake permissions work?

When a moderator is given fake permissions, such as `ban_members`, they will be able to use the `ban` command with **bleh**, but they won't be able to use the native **Discord** ban feature.

### Getting command permissions

You can locate the required permissions for a command with `,help (command)`.

<Frame>
  <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/moderation/permissions.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=b0b1985817e0d410fa9bc0c4791c8722" width="529" height="324" data-path="images/security/moderation/permissions.png" />
</Frame>

### Setting up fake permissions

<Warning>
  The following commands can only be used by the **server owner**.
</Warning>

<AccordionGroup>
  <Accordion title="Granting fake permissions to a role">
    Use the `fakepermissions add` command to grant a fake permission to a role.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,fakepermissions add (role) (permissions)
      ```

      ```javascript Example theme={null}
      ,fakepermissions add @admin ban_members, kick_members
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Revoking fake permissions from a role">
    Use the `fakepermissions remove` command to revoke a fake permission from a role.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,fakepermissions remove (role) (permissions)
      ```

      ```javascript Example theme={null}
      ,fakepermissions remove @admin ban_members, kick_members
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Viewing fake permissions">
    Use the `fakepermissions list` command to view all fake permissions.
    <Info>You can optionally specify a role to only view the fake permissions of that role.</Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,fakepermissions list <role>
      ```

      ```javascript Example theme={null}
      ,fakepermissions list @admin
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Revoking all fake permissions">
    Use the `fakepermissions reset` command to reset all fake permissions.
  </Accordion>
</AccordionGroup>

## Recommended Configuration

<Tabs>
  <Tab title="Moderator">
    * `manage_messages` - Allows the moderator to delete messages.
    * `moderate_members` - Allows the moderator to timeout members.
    * `manage_nicknames` - Allows the moderator to change nicknames.
    * `kick_members` - Allows the moderator to kick members from the server.

    ```javascript theme={null}
    ,fakepermissions grant (moderator role) manage_messages, moderate_members, manage_nicknames, kick_members
    ```
  </Tab>

  <Tab title="Administrator">
    * `manage_messages` - Allows the administrator to delete messages.
    * `moderate_members` - Allows the administrator to timeout members.
    * `manage_nicknames` - Allows the administrator to change nicknames.
    * `manage_roles` - Allows the administrator to manage roles.
    * `ban_members` - Allows the administrator to ban members.
    * `kick_members` - Allows the administrator to kick members.

    ```javascript theme={null}
    ,fakepermissions grant (admin role) manage_messages, moderate_members, manage_nicknames, manage_roles, ban_members, kick_members
    ```
  </Tab>

  <Tab title="Co-Owner">
    * `administrator` - Allows the co-owner to use all moderation commands.

    ```javascript theme={null}
    ,fakepermissions grant (co-owner role) administrator
    ```
  </Tab>
</Tabs>
