> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Auto Responders

> Automatically respond to trigger messages.

## Creating an auto responder

You can create an auto responder with the `autoresponder add` command.

<Warning>
  The **trigger** and **response** must be separated by a comma (`,`).
</Warning>

<Tip>
  The `message` parameter can be raw text or an [embed](/resources/scripting) with dynamic [variables](/resources/scripting/variables).
</Tip>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,autoresponder add (trigger, response) [--flags]
  ```

  ```javascript Example theme={null}
  ,autoresponder add welc, welcome to the server!
  ,autoresponder add welc, {embed}$v{title: welcome}$v{description: welcome to the server!}
  ```

  ```javascript Example with flags theme={null}
  ,autoresponder add welc, welcome to the server! --self_destruct 10 --reply
  ,autoresponder add ,welc, welcome to the server! --not_strict --ignore_command_check
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/messages/responder/add.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=43f4150e0e52478ee4576cd3aeaf46ea" width="800" height="789" data-path="images/configuration/messages/responder/add.png" />
</Frame>

### Available flags

The following flags can be used to customize the response

<AccordionGroup>
  <Accordion title="Not strict">
    The `--not_strict` flag will search for the trigger anywhere in the message.
    For example, if the trigger is `hello`, it will respond to `hello there`.
  </Accordion>

  <Accordion title="Self destruct">
    The `--self_destruct` flag schedules the response for deletion after a
    specified time, which must be between `6` and `60` seconds.
  </Accordion>

  <Accordion title="Delete trigger">
    The `--delete` flag will delete the trigger message after the response is
    sent.
  </Accordion>

  <Accordion title="Reply to trigger">
    The `--reply` flag will reply to the trigger message.
  </Accordion>

  <Accordion title="Ignore command check">
    The `--ignore_command_check` flag will allow the responder to trigger even
    if it's a pre-existing command.
  </Accordion>
</AccordionGroup>

## Removing an auto responder

You can remove an auto responder with the `autoresponder remove` command.

<Info>If you're struggling to remove an auto responder, refer to the [selection removal](/resources/syntax#removing-entries-via-id).</Info>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,autoresponder remove (trigger)
  ```

  ```javascript Example theme={null}
  ,autoresponder remove welc
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/messages/responder/remove.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=2e34076e374c2ef715d727c6ac679e3e" width="384" height="176" data-path="images/configuration/messages/responder/remove.png" />
</Frame>

## Restricting auto responders

### Restricting to a channel or role

Toggle exclusive access for an autoresponder to a role or channel with the `autoresponder exclusive` command

<CodeGroup>
  ```javascript Syntax theme={null}
  ,autoresponder exclusive (role or channel) (trigger)
  ```

  ```javascript Example theme={null}
  ,autoresponder exclusive #general lifetime
  ```
</CodeGroup>

<br />

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/messages/responder/role3.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=bcbbe2e396cbd31072b841e1f80c5935" width="524" height="344" data-path="images/configuration/messages/responder/role3.png" />
</Frame>

## Auto Responder Roles

Autoresponder roles are roles that are assigned or removed to members when they say a specific message.

<Warning>It's easy to confuse these commands! Running the `add` command again would undo the functionality of giving members roles.</Warning>

<CodeGroup>
  ```javascript Syntax theme={null}
  ,autoresponder role (add or remove) (role) (trigger)
  ```

  ```javascript Example theme={null}
  ,autoresponder role add Verified Verify
  ```
</CodeGroup>

<Frame>
  <img src="https://mintcdn.com/bleh/ERtszj3Wuzo7WvDX/images/configuration/messages/responder/role2.png?fit=max&auto=format&n=ERtszj3Wuzo7WvDX&q=85&s=75de23a96f10db8138f06929cbe03152" width="489" height="329" data-path="images/configuration/messages/responder/role2.png" />
</Frame>

### Removing an autoresponder role

You can remove an autoresponder role by running the same command again. This action will reverse the previous configuration and remove the assignment or removals of the role

## Related commands

<AccordionGroup>
  <Accordion title="Updating an auto responder">
    You can use the `autoresponder update` command to update an auto responder.
    <Info>This command uses the same syntax as the `autoresponder add` command.</Info>
  </Accordion>

  <Accordion title="Removing all auto responders">
    You can use the `autoresponder reset` command to remove all auto responders.
  </Accordion>

  <Accordion title="Viewing all auto responders">
    You can use the `autoresponder list` command to view all auto responders.
  </Accordion>
</AccordionGroup>
