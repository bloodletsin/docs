> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Webhook

> Relay messages through a webhook with a custom username and avatar.

## What is a webhook?

A webhook is a way to post a message with a custom username and avatar to a channel.

<Info>
  Webhooks support [embeds](/resources/scripting) with dynamic
  [variables](/resources/scripting/variables).
</Info>

## Creating a webhook

You can use the `webhook create` command to create a webhook.

<Info>The webhook identifier is important for referencing the webhook in other commands.</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,webhook create (name)
  ```

  ```javascript Example theme={null}
  ,webhook create daddyhook
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

### Customizing the webhook

If you want to change the webhook's username or avatar, you can open the **Webhooks** tab in the channel's integrations settings.

<Frame>
  
</Frame>

## Sending a message

After creating a webhook, you can use the `webhook send` command to send a message.

<Info>
  If you've forgotten the identifier, you can use the `webhook list` command to
  view all webhooks.
</Info>

<Tip>You can use the `--add` flag to add another embed to the message.</Tip>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,webhook send (identifier) (message) [--add (embed code)]
  ```

  ```javascript Example theme={null}
  ,webhook send 1cc8rax hello
  ,webhook send 1cc8rax {embed}$v{title: hello} --add {embed}$v{title: hi}
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

### Editing the message

You can use the `webhook edit` command to edit a message sent by a webhook.

<CodeGroup>
  ```javascript Syntax theme={null}
  ,webhook edit (message link) (new message)
  ```

  ```javascript Example theme={null}
  ,webhook edit discord.com/.../ hello world
  ```
</CodeGroup>

<br />

<Frame>
  
</Frame>

## Related commands

<AccordionGroup>
  <Accordion title="Deleting a webhook">
    You can use the `webhook delete` command to delete a webhook.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,webhook delete (identifier)
      ```

      ```javascript Example theme={null}
      ,webhook delete 1cc8rax
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Viewing all webhooks">
    You can use the `webhook list` command to view all webhooks.
  </Accordion>
</AccordionGroup>