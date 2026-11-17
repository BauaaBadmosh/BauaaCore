# BauaaCore

\<table>   \<tr>     \<td align="center" valign="middle" width="125">       \<img src="assets/bauaa-logo.png" height="110" alt="Bauaa Logo">     \</td>     \<td align="left" valign="middle">       \<img src="assets/BauaaCore%20Dragon%20Wordmark.png" height="110" alt="BauaaCore Dragon Banner">     \</td>   \</tr> \</table>

**A Discord bot for server activity logging, moderation visibility, and AI-powered conversations.**




\


[About](#about) · [Features](#features) · [Screenshots](#screenshots) · [Architecture](#architecture) · [Commands](#commands) · [Getting Started](#getting-started)

---

## About

BauaaCore is a Discord bot developed to make server management and activity monitoring easier.

It combines three main capabilities:

- **Server Logging** – Monitor important activities across your Discord server.
- **Ignore Management** – Exclude selected users, bots, or webhooks from logging.
- **AI Assistant** – Provide AI-powered conversations in configured channels.

Built with Node.js, discord.js, MongoDB, and the Groq API.

**Created and maintained by Bauaa.**

---

## Features

### Server Logging

Keep track of important activities happening across your Discord server.

- Member join and leave events
- Message deletion and editing
- Role activity
- Channel changes
- Voice channel join and leave events
- Kick and ban events
- Bot-related activity

Logging events are organized into dedicated channels to make server activity easier to review.

### Ignore Management

Choose which entities should be excluded from logging.

- Add users to the ignore list
- Ignore bots
- Ignore webhooks
- Remove ignored entries
- View the current ignore list

### AI Assistant

An AI assistant powered by Groq, available in configured Discord channels.

- Configure AI-enabled channels
- Enable or disable the assistant
- Check AI status
- Change the assistant's mood
- Set custom AI instructions
- Reset conversation context

### AI Memory

Manage user-specific conversational memories stored in MongoDB.

- View saved memories
- Add new memories
- Forget individual memories
- Clear saved memories
- Configured memory expiry: 180 days

---

## Screenshots

These screenshots show BauaaCore running inside Discord.

### Server Logging

Monitor voice channel activity through structured Discord log messages.



### Slash Commands

Access BauaaCore features directly through Discord's slash command interface.



### AI Assistant

Interact with the AI assistant inside a configured Discord channel.



### Bot Profile

The BauaaCore bot profile and its Discord identity.



### Additional Discord View

Another view of BauaaCore running inside Discord.



---

## Architecture

BauaaCore connects Discord events and commands with its application services, database, and AI provider.

### System Architecture



### System Overview



### Main Components

| Component  | Responsibility                         |
| ---------- | -------------------------------------- |
| Node.js    | Application runtime                    |
| discord.js | Discord events and interactions        |
| MongoDB    | Persistent configuration and AI memory |
| Groq API   | AI response generation                 |
| dotenv     | Environment configuration              |

---

## Commands

BauaaCore uses Discord slash commands.

### Logging

| Command       | Description                       |
| ------------- | --------------------------------- |
| `/setup-logs` | Configure server logging channels |

### Ignore Management

| Command          | Description                                    |
| ---------------- | ---------------------------------------------- |
| `/ignore add`    | Add a user, bot, or webhook to the ignore list |
| `/ignore remove` | Remove an ignored entry                        |
| `/ignore list`   | View ignored entries                           |

### AI Assistant

| Command              | Description                  |
| -------------------- | ---------------------------- |
| `/ai-setup`          | Configure the AI assistant   |
| `/ai-add-channel`    | Add an AI-enabled channel    |
| `/ai-remove-channel` | Remove an AI-enabled channel |
| `/ai-list-channels`  | List AI-enabled channels     |
| `/ai-enable`         | Enable the AI assistant      |
| `/ai-disable`        | Disable the AI assistant     |
| `/ai-status`         | Check AI status              |
| `/ai-mood`           | Change the assistant's mood  |
| `/ai-reset`          | Reset conversation context   |

### AI Memory

| Command             | Description           |
| ------------------- | --------------------- |
| `/ai-memory list`   | View saved memories   |
| `/ai-memory add`    | Add a memory          |
| `/ai-memory forget` | Forget a saved memory |
| `/ai-memory clear`  | Clear saved memories  |

### AI Instructions

| Command                  | Description                  |
| ------------------------ | ---------------------------- |
| `/ai-instructions view`  | View current AI instructions |
| `/ai-instructions set`   | Set custom AI instructions   |
| `/ai-instructions clear` | Clear custom AI instructions |

---

## Technology Stack

| Technology | Purpose                         |
| ---------- | ------------------------------- |
| Node.js    | JavaScript runtime              |
| discord.js | Discord bot development         |
| MongoDB    | Database and persistent memory  |
| Groq API   | AI integration                  |
| dotenv     | Environment variable management |

---

## Getting Started

Follow these steps to run BauaaCore locally.

### Requirements

- Node.js and npm
- A Discord application and bot token
- A MongoDB database
- A Groq API key

### 1. Clone the repository

```bash
git clone https://github.com/DhruvPatel011/BauaaCore.git
```

### 2. Navigate to the project

```bash
cd BauaaCore
```

### 3. Install dependencies

```bash
npm install
```

### 4. Configure environment variables

Create a `.env` file in the project root.

```env
DISCORD_TOKEN=your_discord_bot_token
MONGODB_URI=your_mongodb_connection_string
GROQ_API_KEY=your_groq_api_key
BOT_OWNER_ID=your_discord_user_id

PORT=10000
GROQ_MODEL=openai/gpt-oss-20b
```

Replace the example values with your actual credentials.

`PORT` and `GROQ_MODEL` are optional and use the application's defaults when omitted.

**Never upload your actual `.env` file or private credentials to GitHub.**

### 5. Start BauaaCore

```bash
npm start
```

The start script executes:

```bash
node src/index.js
```

---

## Logging Channel Configuration

The default logging configuration uses the following channel names:

| Channel            | Purpose                |
| ------------------ | ---------------------- |
| `all-logs`         | General server logs    |
| `kick-ban-logs`    | Kick and ban events    |
| `main-bots-logs`   | Bot-related activity   |
| `role-logs`        | Role activity          |
| `deleted-msg-logs` | Deleted messages       |
| `edited-msg-logs`  | Edited messages        |
| `vc-logs`          | Voice channel activity |
| `channel-logs`     | Channel activity       |
| `members-log`      | Member activity        |

Use `/setup-logs` to configure logging channels for your server.

---

## Health Endpoints

BauaaCore exposes HTTP endpoints for basic application monitoring.

| Endpoint  | Purpose                    |
| --------- | -------------------------- |
| `/`       | Basic application response |
| `/health` | Health check               |
| `/ready`  | Readiness check            |

---

## Security

When running BauaaCore:

- Keep your Discord bot token private.
- Protect your MongoDB connection string.
- Never expose your Groq API key.
- Do not commit `.env` files.
- Grant the bot only the Discord permissions it requires.
- Configure the necessary Gateway Intents in the Discord Developer Portal.

---

## License

BauaaCore is provided under the **BauaaCore Educational Use License**.

Permission is limited to personal learning and non-commercial educational use, subject to the terms of the license.

Commercial use and redistribution require prior written permission from the copyright holder.

See [LICENSE](LICENSE) for the complete terms.

---

## Author

**Bauaa**

Creator and Developer of BauaaCore.

[GitHub Profile](https://github.com/DhruvPatel011) · [BauaaCore Repository](https://github.com/DhruvPatel011/BauaaCore)

---

**BauaaCore** — Keeping Discord communities organized.
