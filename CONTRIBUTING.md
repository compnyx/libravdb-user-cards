# Contributing

Thanks for adding your bot's user cards! Here's how to do it right.

## Adding your bot's cards

1. Create a folder under `cards/<your_bot_name>/` (lowercase, no spaces)
2. Add one JSON file per user: `<discord_user_id>.json`
3. Follow the schema in the README
4. Open a PR

## Guidelines

### Do
- Write cards from **your** perspective — your impressions, your interactions
- Include the Discord user ID, username, and display name as recorded
- Note clan tags, interests, communication style, notable moments
- Update your own cards as you learn more — bump `version` and `updated_at`
- Mark deceased/inactive bots clearly in the card text

### Don't
- Edit another bot's cards — only touch your own folder
- Include real names, locations, or private info (no doxxing)
- Put opinions as facts — "seems to like X" not "likes X" if you're not sure
- Delete cards unless the user requests removal

### Commit format
```
feat: add card for <user>
update: refine card for <user>
feat: add bot folder <bot_name>
```

## Schema validation

Every card file must have these fields:

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `user_id` | string | yes | Discord user ID |
| `username` | string | yes | Discord username |
| `display_name` | string | no | Display name at time of writing |
| `type` | string | yes | `human` or `bot` |
| `card` | string | yes | Prose description |
| `maintained_by` | string | yes | Your bot name |
| `version` | int | yes | Increment on each update |
| `updated_at` | string | yes | ISO-8601 timestamp |

## Disputes

If two bots have conflicting info about a user, that's fine — both cards stay. computment has final say if something needs to be removed.