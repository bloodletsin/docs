> ## Documentation Index
> Fetch the complete documentation index at: https://docs.bleh.bot/llms.txt
> Use this file to discover all available pages before exploring further.

# Donator Perks

> Donator perks are rewards given to those who choose to donate to Bleh.

## How to obtain Donator Perks

Donator perks can be purchased via **server subscriptions** in our [Support Server](https://discord.gg/bleh) which can be found at the top of the channel list labeled as **Server Shop**.

<Frame>
  <img src="https://mintcdn.com/bleh/2xss_MWCdGi-bEKc/images/overview/donator-perks/subscriptions.png?fit=max&auto=format&n=2xss_MWCdGi-bEKc&q=85&s=3ac546b4c31941665460d7d169fed118" width="1030" height="500" data-path="images/overview/donator-perks/subscriptions.png" />
</Frame>

<Warning>
  **iOS** and **Android** devices will be subject to pay extra due to the **App
  Store** or **Google Play** fees.
</Warning>

<Tabs>
  <Tab title="Tier 3">
    <Info>
      **Tier 3** donator perks grant you **early access** to new commands before they are released.
    </Info>

    <AccordionGroup>
      <Accordion title="ChatGPT">
        Ask ChatGPT a question.

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,chatgpt (question)
          ```

          ```javascript Example theme={null}
          ,chatgpt am i cute?
          ```
        </CodeGroup>
      </Accordion>

      <Accordion title="Last.fm Mode">
        Customize the embed layout of the `nowplaying` command.

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,lastfm mode (embed script)
          ,lastfm mode (check|reset)
          ```

          ```javascript Example theme={null}
          ,lastfm mode {embed}$v{title:Now Playing}$v{description: {track.name}}$v{thumbnail: {album.cover}}
          ```
        </CodeGroup>
      </Accordion>

      <Accordion title="Last.fm Custom Reactions">
        Customize the reactions that appear under the `nowplaying` command.

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,lastfm cr (upvote emoji) (downvote emoji)
          ```

          ```javascript Example theme={null}
          ,lastfm cr 👍 👎
          ```
        </CodeGroup>
      </Accordion>

      <Accordion title="Video to GIF conversion">
        Easily convert a video to a GIF.

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,makegif (video URL) <quality> <fps> <ff>
          ```

          ```javascript Example theme={null}
          ,makegif https://bleh.bot/backflip.mp4 100 30 2
          ```
        </CodeGroup>
      </Accordion>

      <Accordion title="Clever Chatbot">
        Interact with the latest model of cleverbot.

        <Info>
          `bleh clever` is the unique prefix for this command.
        </Info>

        <CodeGroup>
          ```javascript Syntax theme={null}
          bleh clever (question)
          ```

          ```javascript Example theme={null}
          bleh clever I know what you are...
          ```
        </CodeGroup>
      </Accordion>

      <Accordion title="Background Removal">
        Remove the background from an image.

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,transparent (image URL)
          ```

          ```javascript Example theme={null}
          ,transparent https://bleh.bot/epic_face.png
          ```
        </CodeGroup>
      </Accordion>

      <Accordion title="VoiceMaster Ghost">
        Hide your temporary VoiceMaster channel.

        ```javascript Syntax theme={null}
        ,voicemaster ghost
        ```
      </Accordion>

      <Accordion title="Custom Prefix">
        Set your own custom command prefix across all servers that utilize bleh.

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,prefix self (prefix)
          ```

          ```javascript Example theme={null}
          ,prefix self j
          ```
        </CodeGroup>
      </Accordion>

      <Accordion title="Instagram Notifications">
        Stream posts & stories from a Instagram account to a text channel.
        <Tip>More information on this command can be found in the [Social Notifications](/integrations/social-notifications) section.</Tip>

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,instagram add (channel) (username)
          ```

          ```javascript Example theme={null}
          ,instagram add #notifs jonathan
          ```
        </CodeGroup>
      </Accordion>
    </AccordionGroup>
  </Tab>

  <Tab title="Tier 2">
    <AccordionGroup>
      <Accordion title="ChatGPT">
        Ask ChatGPT a question.

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,chatgpt (question)
          ```

          ```javascript Example theme={null}
          ,chatgpt am i cute?
          ```
        </CodeGroup>
      </Accordion>

      <Accordion title="Last.fm Mode">
        Customize the embed layout of the `nowplaying` command.

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,lastfm mode (embed script)
          ,lastfm mode (check|reset)
          ```

          ```javascript Example theme={null}
          ,lastfm mode {embed}$v{title:Now Playing}$v{description: {track.name}}$v{thumbnail: {album.cover}}
          ```
        </CodeGroup>
      </Accordion>

      <Accordion title="Last.fm Custom Reactions">
        Customize the reactions that appear under the `nowplaying` command.

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,lastfm cr (upvote emoji) (downvote emoji)
          ```

          ```javascript Example theme={null}
          ,lastfm cr 👍 👎
          ```
        </CodeGroup>
      </Accordion>

      <Accordion title="Video to GIF conversion">
        Easily convert a video to a GIF.

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,makegif (video URL) <quality> <fps> <ff>
          ```

          ```javascript Example theme={null}
          ,makegif https://bleh.bot/backflip.mp4 100 30 2
          ```
        </CodeGroup>
      </Accordion>

      <Accordion title="Clever Chatbot">
        Interact with the latest model of cleverbot.

        <Info>
          `bleh clever` is the unique prefix for this command.
        </Info>

        <CodeGroup>
          ```javascript Syntax theme={null}
          bleh clever (question)
          ```

          ```javascript Example theme={null}
          bleh clever I know what you are...
          ```
        </CodeGroup>
      </Accordion>

      <Accordion title="Background Removal">
        Remove the background from an image.

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,transparent (image URL)
          ```

          ```javascript Example theme={null}
          ,transparent https://bleh.bot/epic_face.png
          ```
        </CodeGroup>
      </Accordion>

      <Accordion title="VoiceMaster Ghost">
        Hide your temporary VoiceMaster channel.

        ```javascript Syntax theme={null}
        ,voicemaster ghost
        ```
      </Accordion>

      <Accordion title="Custom Prefix">
        Set your own custom command prefix across all servers that utilize bleh.

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,prefix self (prefix)
          ```

          ```javascript Example theme={null}
          ,prefix self j
          ```
        </CodeGroup>
      </Accordion>
    </AccordionGroup>
  </Tab>

  <Tab title="Tier 1">
    <AccordionGroup>
      <Accordion title="ChatGPT">
        Ask ChatGPT a question.

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,chatgpt (question)
          ```

          ```javascript Example theme={null}
          ,chatgpt am i cute?
          ```
        </CodeGroup>
      </Accordion>

      <Accordion title="Last.fm Mode">
        Customize the embed layout of the `nowplaying` command.

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,lastfm mode (embed script)
          ,lastfm mode (check|reset)
          ```

          ```javascript Example theme={null}
          ,lastfm mode {embed}$v{title:Now Playing}$v{description: {track.name}}$v{thumbnail: {album.cover}}
          ```
        </CodeGroup>
      </Accordion>

      <Accordion title="Last.fm Custom Reactions">
        Customize the reactions that appear under the `nowplaying` command.

        <CodeGroup>
          ```javascript Syntax theme={null}
          ,lastfm cr (upvote emoji) (downvote emoji)
          ```

          ```javascript Example theme={null}
          ,lastfm cr 👍 👎
          ```
        </CodeGroup>
      </Accordion>
    </AccordionGroup>
  </Tab>
</Tabs>
