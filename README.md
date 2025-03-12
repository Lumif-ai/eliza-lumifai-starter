# Eliza Lumifai Starter Kit

## Testing with the Lumifai plugin and network locally

You can download and link the Lumifai Eliza plugin by cloning [this repo](https://github.com/Lumif-ai/plugin-eliza-lumifai)

To run the network locally, you can clone [this repo](https://github.com/Lumif-ai/network-workspace) and follow the instructions

## Edit the character files

Open `src/character.ts` to modify the default character. Uncomment and edit.

### Custom characters

To load custom characters instead:
- Use `pnpm start --characters="path/to/your/character.json"`
- Multiple character files can be loaded simultaneously

### Add Lumifai client
```
# in character.ts
import lumifaiPlugin from "@elizaos-plugins/plugin-lumifai";
plugins: [lumifaiPlugin],

# in character.json
plugins: ["@elizaos-plugins/plugin-lumifai"]
```

## Duplicate the .env.example template

```bash
cp .env.example .env
```

\* Fill out the .env file with your own values.

### Add login credentials and keys to .env
```
DISCORD_APPLICATION_ID="discord-application-id"
DISCORD_API_TOKEN="discord-api-token"
...
OPENROUTER_API_KEY="sk-xx-xx-xxx"
...
TWITTER_USERNAME="username"
TWITTER_PASSWORD="password"
TWITTER_EMAIL="your@email.com"
```

## Install dependencies and start your agent

```bash
pnpm i && pnpm start
```
Note: this requires node to be at least version 22 when you install packages and run the agent.
