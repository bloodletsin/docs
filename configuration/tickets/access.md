> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Blacklist & Access

> Control who can open tickets and manage manual attendees.

For more permission control in tickets, you can use the blacklist or allow/deny manual privileges. Blacklisted members or roles **cannot open tickets**. If an option has `Required Roles` configured, those checks also run before the ticket is opened.

***

## Important Notes

Support visibility is controlled per option. If an option does not define support roles, the system falls back to the global ticket staff role configuration. `Allow` and `deny` are strictly for **extra** ticket access on a specific ticket. They do not replace the creator, claimer, or the ticket's built-in support/staff visibility rules.

<Tip>Manual allow entries are preserved through claim and unclaim, denied while the ticket is closed, and restored if the ticket is reopened. Using deny removes that manual access entry entirely.</Tip>

***

## Global Blacklist

<Callout icon="earth" color="#658A95" iconType="regular">These commands apply globally and are not ticket-specific.</Callout>

<AccordionGroup>
  <Accordion title="Blacklist Member" icon="user-minus">
    Toggles a member on or off the ticket blacklist. Blacklisted users cannot open tickets.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,tickets blacklist (member)
      ```

      ```javascript Example theme={null}
      ,tickets blacklist @bryce
      ```
    </CodeGroup>

    <Frame caption="Blacklisting a user.">
      
    </Frame>
  </Accordion>

  <Accordion title="Blacklist Role" icon="users-slash">
    Toggles a role on or off the ticket blacklist. Anyone with a blacklisted role cannot open tickets.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,tickets blacklist (role)
      ```

      ```javascript Example theme={null}
      ,tickets blacklist @jailed
      ```
    </CodeGroup>

    <Frame caption="Blacklisting a role.">
      
    </Frame>
  </Accordion>

  <Accordion title="Blacklist List" icon="list-ol">
    Shows the users and roles that are blacklisted from opening tickets.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,tickets blacklist
      ```
    </CodeGroup>
  </Accordion>
</AccordionGroup>

***

## Manual Ticket Access

<Callout icon="ticket" color="#658A95" iconType="regular">These commands only apply to the ticket they are used in.</Callout>

<AccordionGroup>
  <Accordion title="Allow Member" icon="user-plus">
    Explicitly lets a user view and send messages in the current ticket while it is open.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,tickets allow (member)
      ```

      ```javascript Example theme={null}
      ,tickets allow @bryce
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Allow Role" icon="users-medical">
    Explicitly lets a role view and send messages in the current ticket while it is open.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,tickets allow (role)
      ```

      ```javascript Example theme={null}
      ,tickets allow @Helper
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Allow List" icon="list-ol">
    Shows the extra users and roles that were explicitly allowed into the current ticket.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,tickets allow list
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Deny Member" icon="user-xmark">
    Removes a user's explicit ticket access.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,tickets deny (member)
      ```

      ```javascript Example theme={null}
      ,tickets deny @bryce
      ```
    </CodeGroup>
  </Accordion>

  <Accordion title="Deny Role" icon="users-slash">
    Removes a role's explicit ticket access.

    <CodeGroup>
      ```javascript Syntax theme={null}
      ,tickets deny (role)
      ```

      ```javascript Example theme={null}
      ,tickets deny @Helper
      ```
    </CodeGroup>
  </Accordion>
</AccordionGroup>