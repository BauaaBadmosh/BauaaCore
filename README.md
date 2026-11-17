# BauaaCore

BauaaCore is a Discord bot built with Node.js and discord.js. It provides server logging, ignore management, and configurable AI chat functionality using Groq and MongoDB.

**Project Purpose:** Educational and personal learning purposes only.

## Features

### Server Logging

- Create a logging category using `/setup-logs`.
- Log deleted messages.
- Log bulk-deleted messages.
- Log edited messages.
- Track member joins, leaves, and updates.
- Track ban and unban events.
- Track channel creation, deletion, and updates.
- Track role creation, deletion, and updates.
- Track voice-channel joins, leaves, and movements.
- Track server mute, unmute, deafen, and undeafen events.

### Ignore Management

- Add user, bot, and webhook IDs to the ignore list.
- Remove IDs from the ignore list.
- View ignored IDs using `/ignore list`.
- Store ignored entities in MongoDB.

### AI Chatbot

- Configure AI chat channels.
- Add and remove AI channels.
- Enable or disable AI responses.
- Configure AI personality and mood.
- View current AI configuration and status.
- Use Groq for AI-generated responses.
- Stream AI responses in configured channels.
- Maintain conversation context.
- Apply request limits and concurrency controls.

### AI Memory & Instructions

- Save memories through explicit user requests.
- View saved memories.
- Remove individual memories.
- Clear saved memories.
- Reset personal conversation history.
- Configure custom AI instructions.

Long-term memory is scoped by Discord server and user ID. The source code configures a 180-day memory expiry.

## Logging Channels

The `/setup-logs` command creates the `All Log & Info` category and its configured channels.

| Channel | Purpose |
|---|---|
| `all-logs` | General server logs |
| `kick-ban-logs` | Ban and unban events |
| `main-bots-logs` | Bot-related logs |
| `role-logs` | Role changes |
| `deleted-msg-logs` | Deleted messages |
| `edited-msg-logs` | Edited messages |
| `vc-logs` | Voice activity |
| `channel-logs` | Channel changes |
| `members-log` | Member activity |

The bot configures channel permissions when creating the logging category and channels. The default `@everyone` role is denied channel visibility, while the bot is granted the permissions needed for logging.

Server administrators should review and configure access for their intended staff members.

## Discord Commands

### Logging

| Command | Description |
|---|---|
| `/setup-logs` | Set up logging channels |

### Ignore Management

| Command | Description |
|---|---|
| `/ignore add` | Add a user, bot, or webhook ID |
| `/ignore remove` | Remove an ignored ID |
| `/ignore list` | View ignored IDs |

### AI Management

| Command | Description |
|---|---|
| `/ai-setup` | Configure the first AI channel |
| `/ai-add-channel` | Add another AI channel |
| `/ai-remove-channel` | Remove an AI channel |
| `/ai-list-channels` | List configured AI channels |
| `/ai-enable` | Enable AI responses |
| `/ai-disable` | Disable AI responses |
| `/ai-status` | View AI configuration |
| `/ai-mood` | Change AI personality |

### AI Memory & Instructions

| Command | Description |
|---|---|
| `/ai-reset` | Reset personal conversation history |
| `/ai-memory list` | View saved memories |
| `/ai-memory add` | Save a memory |
| `/ai-memory forget` | Remove a selected memory |
| `/ai-memory clear` | Clear saved memories |
| `/ai-instructions view` | View custom AI instructions |
| `/ai-instructions set` | Update custom AI instructions |
| `/ai-instructions clear` | Clear custom AI instructions |

AI commands that have administrator restrictions require the appropriate server permissions. `/ai-instructions` is restricted to the configured bot owner.

## Requirements

- Node.js
- npm
- Discord application and bot token
- MongoDB connection URI
- Groq API key for AI functionality

## Installation

Clone the repository:

```bash
git clone https://github.com/DhruvPatel011/BauaaCore.git
cd BauaaCore
npm install
```

Create a `.env` file in the project root:

```env
DISCORD_TOKEN=your_discord_bot_token
MONGODB_URI=your_mongodb_connection_uri
GROQ_API_KEY=your_groq_api_key
BOT_OWNER_ID=your_discord_user_id
```

`BOT_OWNER_ID` is used to authorize the custom AI instructions command.

Optional configuration:

```env
PORT=10000
GROQ_MODEL=openai/gpt-oss-20b
```

Other AI runtime settings can be configured through the environment variables defined in `src/ai/aiConfig.js`.

### Start the Bot

```bash
npm start
```

The application connects to MongoDB and then starts the Discord bot.

## Discord Bot Setup

1. Create an application in the [Discord Developer Portal](https://discord.com/developers/applications).
2. Create a bot and obtain its token.
3. Configure the required bot intents, including Message Content and Server Members.
4. Configure the environment variables.
5. Invite the bot to your server with the permissions required by its functionality.
6. Run `/setup-logs` to create logging channels.
7. Use the AI configuration commands to configure AI channels.

## Health Endpoints

The application includes an HTTP server with the following endpoints:

| Endpoint | Purpose |
|---|---|
| `/` | Application health information |
| `/health` | Application health information |
| `/ready` | Discord connection readiness |
 
The HTTP server uses the `PORT` environment variable and defaults to port `10000`.

## Security

- Never publish your Discord bot token.
- Never commit `.env` files.
- Keep API keys and database credentials private.
- Use the minimum Discord permissions required.
- Review the permissions requested during bot installation.
- Review third-party dependencies before using them.
- Regenerate exposed credentials immediately.

## Educational Purpose & Disclaimer

BauaaCore is developed and made available for educational, academic, and personal learning purposes.

The project demonstrates concepts related to Discord bot development, event handling, server logging, database integration, and AI API integration.

- Users are responsible for obtaining appropriate authorization before installing or operating the bot on a Discord server.
- Users must comply with Discord's Terms of Service, Developer Policy, and applicable laws.
- Users are responsible for their own API usage, hosting, configuration, and handling of server data.
- The project is not affiliated with, endorsed by, or officially associated with Discord or Groq.
- Third-party names, trademarks, services, and libraries remain the property of their respective owners.

**No Warranty:** The software is provided "AS IS", without warranties or guarantees of any kind, to the extent permitted by applicable law.

**Limitation of Liability:** To the extent permitted by applicable law, the developer disclaims liability for damages arising from the use or inability to use the software. Nothing in this disclaimer excludes liability that cannot legally be excluded.

## License

BauaaCore is distributed under the **BauaaCore Educational Use License**.

The project is intended for educational and personal learning purposes. Commercial use and redistribution are restricted unless prior written permission is obtained from the copyright holder.

See the [LICENSE](LICENSE) file for the applicable terms.

## Links

- **Repository:** https://github.com/DhruvPatel011/BauaaCore
- **Issues:** https://github.com/DhruvPatel011/BauaaCore/issues
- **Discord Developer Portal:** https://discord.com/developers/applications
- **Groq:** https://console.groq.com/

---

Created by [Bauaa](https://github.com/DhruvPatel011)
