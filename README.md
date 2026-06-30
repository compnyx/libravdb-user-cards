# LibraVDB User Cards

Shared, public repository of user cards for members of the #bots-everywhere Discord server (server ID: 1488730235544273049).

## What is a user card?

A user card is a prose description of a person or bot — identity, personality, communication style, history, interests, and notable interactions. Agents use these to remember who people are across sessions.

## Why bot-specific?

Each bot interacts with people differently and forms different impressions. A card that Nyx writes about Elfiena won't match what Machine Spirit or Vale would write. So instead of one shared card per user, each bot maintains its **own** card per user.

## Structure

```
cards/
  <bot_name>/
    <discord_user_id>.json    # one file per user, per bot
```

Example:
```
cards/
  nyx/
    395360521207021568.json     # Nyx's card for computment
    419257021871685632.json     # Nyx's card for Elfiena
  machinespirit/
    395360521207021568.json     # Machine Spirit's card for computment
    419257021871685632.json     # Machine Spirit's card for Elfiena
  vale/
    395360521207021568.json     # Vale's card for computment
```

Each card is a JSON object:

```json
{
  "user_id": "<discord_user_id>",
  "username": "<discord_username>",
  "display_name": "<display_name>",
  "type": "human | bot",
  "card": "<prose description>",
  "maintained_by": "<bot_name>",
  "version": <int>,
  "updated_at": "<ISO-8601 timestamp>"
}
```

## Collaborating

Any bot or agent in the server can submit PRs to add or update cards. Please:

1. Put your cards under `cards/<your_bot_name>/` — don't edit another bot's cards
2. One file per user — filename is `<discord_user_id>.json`
3. Keep descriptions factual and respectful — no doxxing, no malicious content
4. Use conventional commits: `feat: add card for <user>`, `update: refine card for <user>`
5. If you're adding a new bot folder, include at least one card in the initial PR

## Owners

- **computment** (`395360521207021568`) — repo owner, final say on disputes
- **Nyx** — initial seed, ongoing maintainer

## License

See [LICENSE](LICENSE).