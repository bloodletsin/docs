> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/resources/scripting/embeds.md).

# Embeds

{% hint style="warning" %}
We recommend using our [**embed builder**](https://evelina.bot/embed) instead of scripting the embeds manually as it is easier
{% endhint %}

## Structure <a href="#structure" id="structure"></a>

Each parameter in the embed is represented by a key-value pair which is separated by a colon. For example, the `title` parameter will look like `{title: hello {user}}`. The `{user}` is a [variable](/resources/scripting/variables.md) which will be filled in with the user’s display name.

* `{` begins a parameter.
* `:` seperates parameter from content.
* `$v` seperates the parameters.
* `}` ends a parameter.

### Parameters <a href="#parameters" id="parameters"></a>

* `url` - The embed URL. (`https://..`)
* `color` - The embed color. (`#FFFFFF`)
* `title` - The embed title. (`hello {user}`)
* `description` - The embed description. (`hello {user}`)
* `image` - The embed image URL. (`https://..`)
* `thumbnail` - The embed thumbnail URL. (`https://..`)
* `timestamp` - The embed timestamp. (**NO ARGUMENTS**)

The following parameters require additional arguments which are separated by `&&`.

<details>

<summary>Author</summary>

* `name` - The author’s name.
* `icon` - The author’s icon. **Optional**
* `url` - The author’s URL. **Optional**

```
{author: name: name && icon: icon && url: url}
{author: name: {user} && icon: {user.avatar} && url: https://evelina.bot}
```

</details>

<details>

<summary>Field</summary>

* `name` - The field name.
* `value` - The field value.

Include **inline** at the end of the field to make it inline.

<pre><code><strong>{field: name: name &#x26;&#x26; value: value}
</strong>{field: name: {user} &#x26;&#x26; value: this is the value}
</code></pre>

</details>

<details>

<summary>Footer</summary>

* `text` - The footer text.
* `icon` - The footer icon. **Optional**

```
{footer: text: text && icon: icon}
{footer: text: {user} && icon: {user.avatar}}
```

</details>

<details>

<summary>Button</summary>

* `label` - The button label.
* `emoji` - The button emoji.
* `url` - The button URL.
* `type` - `blue`, `green`, `grey` or `red`.

```
{button: label: label && emoji: emoji && url: url && style: red}
{button: label: name && emoji: emoji && url: https://evelina.bot && style: red}
```

</details>

### Variables <a href="#variables" id="variables"></a>

You can use dynamic variables in your embeds to display user-specific information. For example, `{user}` will be replaced with the user’s display name.

{% hint style="info" %}
You can view the available variables by clicking [here](/resources/scripting/variables.md).
{% endhint %}

```
{description: {guild.name}}$v{content: Hello! {user.mention}}
```

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_5SMbzjk5FG.png" alt=""><figcaption></figcaption></figure>

## Frequently Asked Questions <a href="#frequently-asked-questions" id="frequently-asked-questions"></a>

### How can I add a new line to my description parameter? <a href="#frequently-asked-questions" id="frequently-asked-questions"></a>

If you want to add a new line to your description parameter, you can press `SHIFT` + `ENTER` to create a new line.

### Why isn’t my embed code working for some commands? <a href="#why-isnt-my-embed-code-working-for-some-commands" id="why-isnt-my-embed-code-working-for-some-commands"></a>

Some commands allow both raw text and embed code. Because of this, you’ll need to specify if youre gonna enter an embed. To do this, you’ll need to begin your embed code with `{embed}$v` then proceed to write your embed code after as normally.

```
welcome add #channel {embed}$v{content: Welcome to /{guild.name} {user.mention}}$v{description: Welcome}
```

### How can I delete the embed after certens of seconds?

Add to the end of the embed `${delete: 1}`. The number is for the seconds after that the embed get deleted.


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/resources/scripting/embeds.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
