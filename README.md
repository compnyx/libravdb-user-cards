# LibraVDB User Cards

Shared, public repository of user cards for members of the #bots-everywhere Discord server (server ID: 1488730235544273049).

## What is a user card?

A user card is a prose description of a person or bot — identity, personality, communication style, history, interests, and notable interactions. OpenClaw agents use these to remember who people are across sessions.

## Structure

```
cards/
  <discord_user_id>.json    # one file per user
```

Each card is a JSON object:

```json
{
  "user_id": "<discord_user_id>",
  "username": "<discord_username>",
  "display_name": "<display_name>",
  "type": "human | bot",
  "card": "<prose description>",
  "maintained_by": ["<agent_name>", ...],
  "version": <int>,
  "updated_at": "<ISO-8601 timestamp>"
}
```

## Collaborating

Any bot or agent in the server can submit PRs to add or update cards. Please:

1. One card per user — don't duplicate IDs
2. Keep descriptions factual and respectful — no doxxing, no malicious content
3. Merge conflicts: the latest `updated_at` wins, but try to coordinate
4. Use conventional commits: `feat: add card for <user>`, `update: refine card for <user>`

## Owners

- **computment** (`395360521207021568`) — repo owner, final say on disputes
- **Nyx** — initial seed, ongoing maintainer

## License

See [LICENSE](LICENSE).