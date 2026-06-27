> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Pagination

> Guide to paginating embeds with bleh.

## Setup

<Warning>Only embeds created with `createembed` can be paginated.</Warning>

<Steps>
  <Step title="Set the embed">
    Firstly you must set the embed to work with pagination. `,pagination set     [message link]` <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/resources/scripting/pagination/set.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=e064c90b7f4c8f3786fbce1d5b3a5aac" alt="pn set" width="702" height="415" data-path="images/resources/scripting/pagination/set.png" />
  </Step>

  <Step title="Add the next page">
    You can now add further pages to your embed. This command works with adding
    any number of pages required. `,pagination add [message link] [embed
            content]` <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/resources/scripting/pagination/add.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=6586ce6e9588f4c669491faee179e3fb" alt="pn add" width="771" height="417" data-path="images/resources/scripting/pagination/add.png" />
  </Step>

  <Step title="Updating a paginated embed">
    If you need to edit a page you've made during setup, you can use the command
    below. `,pagination update [message link] [page number]` <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/resources/scripting/pagination/update.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=0185c856efe1ceaa2562d8e2b87e323d" alt="pn
    update" width="838" height="632" data-path="images/resources/scripting/pagination/update.png" />
  </Step>

  <Step title="Removing a page">
    If you want to remove a page you have setup, you can use the below command
    `,pagination remove [message link] [page number]` <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/resources/scripting/pagination/remove.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=b4da64a32dfbfc620aa3eebe2ab1a47f" alt="pn
    del" width="684" height="411" data-path="images/resources/scripting/pagination/remove.png" />
  </Step>
</Steps>

## Related commands

<AccordionGroup>
  <Accordion title="Delete a paginated embed entirely">
    ```
    ,pagination delete [message link]
    ```
  </Accordion>

  {" "}

  <Accordion title="Reset all paginated embeds in a guild">
    `,pagination reset`
  </Accordion>

  <Accordion title="List all active paginations">
    ```
    ,pagination list
    ```
  </Accordion>

  <Accordion title="Readd the navigation reactions">
    Use this command in case the arrow reactions allowing navigation between pages were deleted.

    ```
    ,pagination restorereactions (message link)
    ```
  </Accordion>
</AccordionGroup>
