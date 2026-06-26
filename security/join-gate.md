> For the complete documentation index, see [llms.txt](https://docs.bleh.rest/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.bleh.rest/security/join-gate.md).

# Join Gate

## Configuring the antiraid system

### Preventing mass joins <a href="#preventing-mass-joins" id="preventing-mass-joins"></a>

This module will trigger when the number of accounts joining the server exceeds the threshold within a short time frame.

```
Syntax: ;antiraid massjoin enable [punishment] [threshold]
Example: ;antiraid massjoin enable ban 3
```



### Requiring an avatar <a href="#requiring-an-avatar" id="requiring-an-avatar"></a>

This module will trigger when an account joins the server without an avatar.

```
Syntax: ;antiraid avatar enable [punishment]
Example: ;antiraid avatar enable ban
```



### Setting a minimum account age

This module will trigger when an account joins the server that is younger than the specified age.



### Exempting accounts from the antiraid <a href="#exempting-accounts-from-the-antiraid" id="exempting-accounts-from-the-antiraid"></a>

You can exempt accounts from the antiraid with the `antiraid whitelist` command.





## Viewing the antiraid configuration <a href="#viewing-the-antiraid-configuration" id="viewing-the-antiraid-configuration"></a>

You can use the `antiraid config` command to view the current antiraid configuration.
