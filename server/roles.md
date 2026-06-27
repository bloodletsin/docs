> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Booster Roles

> Reward your boosters with unique roles for themselves.

## What are booster roles?

Booster roles are unique roles that are given to members which have boosted your server. These roles can be fully customized by the members themselves.

## Setting the base role

In order for the booster roles to work, you must set a base role. All booster roles will be placed under this role.

<Tip>The base role should be a role which is above any roles with a color, otherwise the color won't be visible due to Discord's role hierarchy.</Tip>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,boosterrole base (role)
  ```

  ```javascript Example theme={null}
  ,boosterrole base @------
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/roles/booster/base-position.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=69530273dbb7d4126fe46d57a81021ec" width="419" height="203" data-path="images/configuration/roles/booster/base-position.png" />
</Frame>

## Creating a booster role

You can create a booster role by using the `boosterrole` command itself.

<Info>The `color` parameter can be a hex code or a color name.</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,boosterrole (color) <name>
  ```

  ```javascript Example theme={null}
  ,boosterrole #3498DB boss
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/roles/booster/create.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=ed19a5fab4e276d531c673ea89fb02fd" width="611" height="171" data-path="images/configuration/roles/booster/create.png" />
</Frame>

## Customizing your booster role

### Changing the name

You can use the `boosterrole rename` command to change the name of your booster role.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,boosterrole rename (new name)
  ```

  ```javascript Example theme={null}
  ,boosterrole rename boss role
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/roles/booster/rename.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=32dd493db9b9a4e5433b63de8964c95f" width="532" height="170" data-path="images/configuration/roles/booster/rename.png" />
</Frame>

### Changing the icon

You can use the `boosterrole icon` command to change the icon of your booster role.

<Info>You can use an emoji or an attachment.</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,boosterrole icon (emoji or attachment)
  ```

  ```javascript Example theme={null}
  ,boosterrole icon :cool:
  ,boosterrole icon https://bleh.bot/bleh.png
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/roles/booster/icon.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=02914bfd9e092274b5bfc9523e076a8f" width="476" height="506" data-path="images/configuration/roles/booster/icon.png" />
</Frame>

## Removing your booster role

If you no longer want your booster role, you can use the `boosterrole remove` command.

## Automatically grant a role to boosters

You can reward your boosters with a role upon boosting your server. You can use the `boosterrole award` command to set this up.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,boosterrole award (role)
  ```

  ```javascript Example theme={null}
  ,boosterrole award @immunity
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/roles/booster/award.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=6bbef20cb67b922f629e627b3105993f" width="432" height="168" data-path="images/configuration/roles/booster/award.png" />
</Frame>

### Viewing the role being awarded

You can use the `boosterrole award view` command to view the role being awarded.

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/roles/booster/award-view.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=91ed94dd4f9b6317a3064c7c890884ec" width="461" height="168" data-path="images/configuration/roles/booster/award-view.png" />
</Frame>

### Removing the role being awarded

You can use the `boosterrole award remove` command to remove the role being awarded.

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/roles/booster/award-remove.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=572f4489b66e95843373932cefc2f2fe" width="416" height="165" data-path="images/configuration/roles/booster/award-remove.png" />
</Frame>

## Related commands

<AccordionGroup>
  <Accordion title="Viewing all booster roles">
    You can use the `boosterrole list` command to view all booster roles.
  </Accordion>

  <Accordion title="Cleaning up booster roles">
    You can use the `boosterrole cleanup` command if they weren't removed
    properly.
  </Accordion>
</AccordionGroup>
