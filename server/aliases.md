> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Command Aliases

> Create shortcuts to invoke other commands.

## Overview

Command aliases allow you to create custom commands that run other commands. This can be useful for creating shorter or more memorable commands for your server. For example, you could create an alias that runs the `role` command with a specific role.

## Creating an alias

You can create an alias using the `alias add` command.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,alias add (shortcut) (command)
  ```

  ```javascript Example theme={null}
  ,alias add deport ban
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/aliases/add.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=d239addf8a60eb2bbce6fd4a3a1f86e2" width="547" height="480" data-path="images/configuration/aliases/add.png" />
</Frame>

### Predefined arguments

You're able to use predefined arguments in your aliases, however, if you want to use the user's input as an argument, you have to use `{}`.
Keep in mind that the first argument is `{0}`, the second argument is `{1}`, and so on, it doesn't start at `{1}`.

```javascript theme={null}
,ban @jonathan Harassing Members
// {0} would be @jonathan
// {1} would be Harassing Members
```

Below is an example of an alias that uses predefined arguments:

```javascript theme={null}
,alias add shh timeout {0} 10m
,shh @jonathan
```

This alias would run the `timeout` command with the first argument being `@jonathan` from the user's input and the second argument being `10m` as predefined.

### Making a command to grant image permissions

If you're interested in creating a command that grants image permissions to a user, you can use the following alias which invokes the `role` command with the predefined image role.

```javascript theme={null}
,alias add pic role {0} @image-role
,pic @jonathan
```

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/aliases/add-pic.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=feab82f27b0eed2c91af00006dcfd377" width="459" height="350" data-path="images/configuration/aliases/add-pic.png" />
</Frame>

## Removing an alias

You can remove an alias using the `alias remove` command.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,alias remove (shortcut)
  ```

  ```javascript Example theme={null}
  ,alias remove deport
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/aliases/remove.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=e94113db2bd413f867f272e717b42af1" width="337" height="169" data-path="images/configuration/aliases/remove.png" />
</Frame>

## Related commands

<AccordionGroup>
  <Accordion title="Viewing an alias">
    You can use the `alias view` command to view what an alias invokes.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,alias view (shortcut)
      ```

      ```javascript Example theme={null}
      ,alias view deport
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Viewing all aliases">
    You can use the `alias list` command to view all aliases.
  </Accordion>
</AccordionGroup>
