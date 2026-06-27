> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Antinuke

> Impose restrictions on moderators to prevent destructive behavior.

## Why use an antinuke system?

It's important to have an antinuke system in place to prevent moderators from abusing their permissions. This is a security measure which lets your server stay safe from any harmful actions.

## How does the antinuke work?

The antinuke will set a limit on the number of actions a moderator can perform in a certain time frame. If the limit is exceeded, the moderator will be punished and a message will be sent to the owner.

## Configuring the antinuke

<Warning>
  Discord recently implemented a new **mass ban** feature which can quickly ban
  **100+ members**. It's **HIGHLY** recommended to utilize [fake
  permissions](/security/fake-permissions) to prevent moderators from using this
  feature.
</Warning>

### Allowing users to configure the antinuke

Initially, only the **server owner** can configure the antinuke. However, you can allow other users to configure the antinuke with the `antinuke admin` command.

<Warning>
  This is a dangerous command and will allow the user to entirely alter the
  antinuke configuration.
</Warning>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,antinuke admin (user)
  ```

  ```javascript Example theme={null}
  ,antinuke admin @jonathan
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antinuke/admin.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=2c607b17195ebd51a5dbcccec920dc1c" alt="" width="658" height="371" data-path="images/security/antinuke/admin.png" />
</Frame>

### Exempting users from the antinuke

You can exempt users from the antinuke with the `antinuke whitelist` command.

<Warning>
  This is a dangerous command and will allow the user to bypass the antinuke
  entirely.
</Warning>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,antinuke whitelist (user)
  ```

  ```javascript Example theme={null}
  ,antinuke whitelist @jonathan
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antinuke/whitelist.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=3d0c13568d3c1006003971732d9445db" alt="" width="573" height="346" data-path="images/security/antinuke/whitelist.png" />
</Frame>

## Enabling an antinuke module

### Available Flags

The following flags can be used to define the antinuke module

<AccordionGroup>
  <Accordion title="Threshold">
    The threshold is the number of actions a moderator can perform before being punished.

    <Info>
      It's recommended to keep the threshold between `1` and `6` to stay safe.
    </Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      --threshold (number)
      ```

      ```javascript Example theme={null}
      --threshold 3
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Punishment">
    The punishment which will be applied to the moderator.

    <Info>
      Available punishments can be found in the [punishments](/resources/syntax#flag-punishments) section.
    </Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      --do (punishment)
      ```

      ```javascript Example theme={null}
      --do ban
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Command Detection">
    Whether bleh commands should be counted towards the threshold. (e.g. `,ban`)

    <CodeGroup>
      ```javascript Syntax theme={null}
      --command (on | off)
      ```

      ```javascript Example theme={null}
      --command on
      ```
    </CodeGroup>
  </Accordion>
</AccordionGroup>

### Available Modules

<AccordionGroup>
  <Accordion title="Punishing members for changing the vanity URL">
    You can prevent members from changing the vanity URL with the following command

    <Warning>
      bleh can not change the vanity URL back to the original due to Discord limitations.
    </Warning>

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,antinuke vanity (on or off) [--do (punishment)]
      ```

      ```javascript Example theme={null}
      ,antinuke vanity on --do ban
      ```
    </CodeGroup>

    <br />

    <Frame>
      <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antinuke/vanity.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=a3da459d9d0f3d4d65d39d5aea12b664" alt="" width="590" height="174" data-path="images/security/antinuke/vanity.png" />
    </Frame>
  </Accordion>

  <Accordion title="Preventing bots from being added">
    You can prevent bots from being mass added with the following command

    <Info>
      You'll need to use `antinuke whitelist (bot ID)` to invite bots.
    </Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,antinuke botadd (on or off)
      ```

      ```javascript Example theme={null}
      ,antinuke botadd on
      ```
    </CodeGroup>

    <br />

    <Frame>
      <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antinuke/botadd.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=a4d82d10f8a804705e96b741099cdca3" alt="" width="415" height="174" data-path="images/security/antinuke/botadd.png" />
    </Frame>
  </Accordion>

  <Accordion title="Preventing members from being banned">
    You can prevent members from being mass banned with the following command

    <Info>
      It's recommended to include the `--command on` flag.
    </Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,antinuke ban (on or off) [--threshold (number)] [--do (punishment)] [--command (on | off)]
      ```

      ```javascript Example theme={null}
      ,antinuke ban on --threshold 3 --do ban --command on
      ```
    </CodeGroup>

    <br />

    <Frame>
      <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antinuke/ban.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=26404c754f89bf2b5683ae341cc38781" alt="" width="610" height="193" data-path="images/security/antinuke/ban.png" />
    </Frame>
  </Accordion>

  <Accordion title="Preventing members from being kicked">
    You can prevent members from being mass kicked with the following command

    <Info>
      It's recommended to include the `--command on` flag.
    </Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,antinuke kick (on or off) [--threshold (number)] [--do (punishment)] [--command (on | off)]
      ```

      ```javascript Example theme={null}
      ,antinuke kick on --threshold 3 --do ban --command on
      ```
    </CodeGroup>

    <br />

    <Frame>
      <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antinuke/kick.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=9f4ebf5118e75c60f272cf24594794cd" alt="" width="616" height="189" data-path="images/security/antinuke/kick.png" />
    </Frame>
  </Accordion>

  <Accordion title="Preventing roles from being deleted">
    You can prevent roles from being mass deleted with the following command

    <Info>
      It's recommended to include the `--command on` flag.
    </Info>

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,antinuke role (on or off) [--threshold (number)] [--do (punishment)] [--command (on | off)]
      ```

      ```javascript Example theme={null}
      ,antinuke role on --threshold 3 --do ban --command on
      ```
    </CodeGroup>

    <br />

    <Frame>
      <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antinuke/role.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=af70263d33fc8caa6011f18457eab8cf" alt="" width="611" height="194" data-path="images/security/antinuke/role.png" />
    </Frame>
  </Accordion>

  <Accordion title="Preventing channels from being created or deleted">
    You can prevent channels from being mass created or deleted with the following command

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,antinuke channel (on or off) [--threshold (number)] [--do (punishment)]
      ```

      ```javascript Example theme={null}
      ,antinuke channel on --threshold 3 --do ban
      ```
    </CodeGroup>

    <br />

    <Frame>
      <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antinuke/channel.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=efa5138c97745fd3f384e1885ec05f03" alt="" width="440" height="191" data-path="images/security/antinuke/channel.png" />
    </Frame>
  </Accordion>

  <Accordion title="Preventing emojis from being deleted">
    You can prevent emojis from being mass deleted with the following command

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,antinuke emoji (on or off) [--threshold (number)] [--do (punishment)]
      ```

      ```javascript Example theme={null}
      ,antinuke emoji on --threshold 3 --do ban
      ```
    </CodeGroup>

    <br />

    <Frame>
      <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antinuke/emoji.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=eb1629eabf5ac3fce204fb231eddd45b" alt="" width="451" height="192" data-path="images/security/antinuke/emoji.png" />
    </Frame>
  </Accordion>

  <Accordion title="Preventing webhooks from being created">
    You can prevent webhooks from being mass created with the following command

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,antinuke webhook (on or off) [--threshold (number)] [--do (punishment)]
      ```

      ```javascript Example theme={null}
      ,antinuke webhook on --threshold 3 --do ban
      ```
    </CodeGroup>

    <br />

    <Frame>
      <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antinuke/webhook.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=4fdfa6219ce5a26aea2a92d47012962e" alt="" width="446" height="192" data-path="images/security/antinuke/webhook.png" />
    </Frame>
  </Accordion>
</AccordionGroup>

## Disabling an antinuke module

You can disable an antinuke module with the same command you used to enable it, but with the status set to `off`.

## Viewing the antinuke configuration

You can use the `antinuke config` command to view the current antinuke configuration.

<Frame>
  <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antinuke/config.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=c446e9579d51bf376b7a66d6b67af7b2" alt="" width="590" height="408" data-path="images/security/antinuke/config.png" />
</Frame>

### Viewing the modules & whitelist

You can use the `antinuke list` command to view the enabled modules and whitelisted users.

<Frame>
  <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antinuke/list.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=07d2e85b4ddd0f20cb79c00afcf9e3aa" alt="" width="572" height="496" data-path="images/security/antinuke/list.png" />
</Frame>

### Viewing users with antinuke admin

You can use the `antinuke admins` command to view users which can configure the antinuke.

<Frame>
  <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/security/antinuke/admins.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=124a9e5b847736ca33ea362b900ce06c" alt="" width="291" height="307" data-path="images/security/antinuke/admins.png" />
</Frame>

### Permissions available for `antinuke permissions (grant or remove)`

| Antinuke Permissions |
| -------------------- |
| `administrator`      |
| `ban_members`        |
| `mention_everyone`   |
| `kick_members`       |
| `moderate_members`   |
| `manage_guild`       |
| `manage_channels`    |
| `manage_roles`       |
| `view_audit_log`     |
| `manage_webhooks`    |
| `manage_expressions` |
| `manage_nicknames`   |
