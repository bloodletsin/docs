> For the complete documentation index, see [llms.txt](https://docs.evelina.bot/llms.txt). Markdown versions of documentation pages are available by appending `.md` to page URLs; this page is available as [Markdown](https://docs.evelina.bot/integrations/last.fm.md).

# Last.fm

## What is Last.fm? <a href="#what-is-last-fm" id="what-is-last-fm"></a>

Last.fm is a website which tracks the music you listen to and provides statistics based on your listening history. You can register for a Last.fm account by clicking [here](https://www.last.fm/join).

## Creating a Last.fm account

{% stepper %}
{% step %}

#### Registration

Visit the [last.fm registration page](https://www.last.fm/join) and fill in the required information.
{% endstep %}

{% step %}

#### Verification

Verify your email address by clicking the link sent to your [inbox](https://gmail.com/).
{% endstep %}
{% endstepper %}

After creating your account, you’ll likely want to connect your **Spotify account** to automatically scrobble your listening activity. You can do this by visiting the [Last.fm connections](https://www.last.fm/settings/applications) page and clicking the **Connect** button next to **Spotify Scrobbling**.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/spotify-scrobbling.png" alt=""><figcaption></figcaption></figure>

## Connecting your Last.fm account <a href="#connecting-your-last-fm-account" id="connecting-your-last-fm-account"></a>

Use the `lastfm login` command, and follow the instructions.

<figure><img src="https://github.com/EvelinaServices/docs/blob/main/.gitbook/assets/Discord_NAvczjo90k.png" alt=""><figcaption></figcaption></figure>

## Known Issues <a href="#known-issues" id="known-issues"></a>

### Out of Sync

**Last.fm** and **Spotify** struggle to stay in sync, causing outdated information to be displayed.

* Restart your **Spotify application** to force a refresh.
* Disconnect and reconnect your **Spotify account** in the [Last.fm connections](https://www.last.fm/settings/applications).

### Last.fm Failure <a href="#last-fm-failure" id="last-fm-failure"></a>

If you see an unexpected error message, it’s possible that **Last.fm** is currently down.

* Check the [Last.fm status page](https://status.last.fm/) for more information.
* If the issue persists, please join our [support server](https://discord.gg/evelina) for further assistance.


---

# Agent Instructions
This documentation is published with GitBook. GitBook is the documentation platform designed so that both humans and AI agents can read, navigate, and reason over technical content effectively. Learn more at gitbook.com.

## Querying This Documentation
If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter, and the optional `goal` query parameter:

```
GET https://docs.evelina.bot/integrations/last.fm.md?ask=<question>&goal=<endgoal>
```

`ask` is the immediate question: it should be specific, self-contained, and written in natural language.
`goal` is optional and describes the broader end goal you are ultimately trying to accomplish on behalf of the user. GitBook uses it to tailor the answer towards what is most useful for that goal.

The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
