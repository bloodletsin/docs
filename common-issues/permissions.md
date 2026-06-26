> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Permissions

> How to solve channel permission issues.

## Text Channel Permissions

Usually, if members are still able to send messages in a text channel after being muted, it is likely because of the `@everyone` channel permissions being set incorrectly.

<Steps>
  <Step title="Set the channel permissions">
    Go to your channel settings, and navigate to the **Permissions** tab.
    Find the `@everyone` or **member** role and ensure that the **Send Messages** permission is set to **Neutral** (`/`).

    <Frame>
      <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/common-issues/channel-permission.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=f2a6898fe3e57aded62e959f17721718" className="w-auto" width="689" height="274" data-path="images/common-issues/channel-permission.png" />
    </Frame>
  </Step>

  <Step title="Check server wide role permissions">
    Go to your server settings, and navigate to the **Roles** tab.
    Find the `@everyone` or **member** role and ensure that the **Send Messages** permission isn't enabled.

    <Frame>
      <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/common-issues/server-role-permission.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=87b07b1e2f57ed45411b61a2888fe018" className="w-auto" width="471" height="294" data-path="images/common-issues/server-role-permission.png" />
    </Frame>
  </Step>

  <Step title="Check for role overrides">
    Check if there are any roles that have permission overrides for the channel in question. If a role has the **Send Messages** permission enabled, it will override the `@everyone` permissions and allow members to send messages.
  </Step>
</Steps>

### Lockdown Command

If you have a custom member role instead of the default `@everyone` role, make sure that the lockdown command is set to restrict that role instead of the `@everyone` role.
<Tip>The steps above are also required for the lockdown command to work properly.</Tip>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,lockdown role (role)
  ```

  ```javascript Example theme={null}
  ,lockdown role @Member
  ```
</CodeGroup>

## Voice Channel Permissions

If your VoiceMaster channels aren't working as expected due to permission issues, you can use the **category** to manage permissions for all channels within it.