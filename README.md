# BauaaCore

A Discord bot for server logging, moderation tracking, and AI-powered conversations.

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Discord.js-5865F2?style=flat&logo=discord&logoColor=white" alt="Discord.js">
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white" alt="MongoDB">
  <img src="https://img.shields.io/badge/Groq_AI-F55036?style=flat" alt="Groq AI">
</p>

---

## About

BauaaCore is a Discord bot built to make server management easier. It handles server activity logs, keeps track of moderation events, and provides an AI assistant that can be used in selected channels.

The bot uses MongoDB to store configuration and AI memory, so important information can be retained between restarts.

## Features

### Server Logging
Keep track of important activities happening across your Discord server.

- Member join and leave events
- Message deletion and editing
- Role creation, deletion and updates
- Channel changes
- Voice channel activity
- Kick and ban events
- Bot-related activity

Logs can be organized into separate channels to make server activity easier to review.

### Ignore Management

Not every event needs to appear in your logs. The ignore system lets you exclude specific entities from logging.

- Ignore users
- Ignore bots
- Ignore webhooks
- View and manage ignored entries

### AI Assistant

BauaaCore also includes an AI assistant powered by the Groq API.

- Enable AI in selected channels
- Add or remove AI-enabled channels
- Configure the assistant's mood and instructions
- Enable or disable AI whenever needed
- Reset conversation context
- Check the current AI status

### AI Memory

The assistant can retain user-specific information using MongoDB.

You can add, view, forget, or clear saved memories through slash commands. Stored memories are configured with a 180-day expiry.

---

## Commands

All commands are available through Discord slash commands.

### Logging

| Command | Description |
|---|---|
| `/setup-logs` | Configure server logging channels |

### Ignore Management

| Command | Description |
|---|---|
| `/ignore add` | Add a user, bot, or webhook to the ignore list |
| `/ignore remove` | Remove an entry from the ignore list |
| `/ignore list` | View ignored entries |

### AI Assistant

| Command | Description |
|---|---|
| `/ai-setup` | Configure the AI assistant |
| `/ai-add-channel` | Allow AI in a channel |
| `/ai-remove-channel` | Remove AI access from a channel |
| `/ai-list-channels` | View AI-enabled channels |
| `/ai-enable` | Enable the AI assistant |
| `/ai-disable` | Disable the AI assistant |
| `/ai-status` | Check the current AI status |
| `/ai-mood` | Change the assistant's mood |
| `/ai-reset` | Reset conversation context |

### AI Memory

| Command | Description |
|---|---|
| `/ai-memory list` | View saved memories |
| `/ai-memory add` | Add a memory |
| `/ai-memory forget` | Forget a saved memory |
| `/ai-memory clear` | Clear saved memories |

### AI Instructions

| Command | Description |
|---|---|
| `/ai-instructions view` | View current instructions |
| `/ai-instructions set` | Set custom instructions |
| `/ai-instructions clear` | Clear custom instructions |

---

## Technology

BauaaCore is built using the following technologies:

- **Node.js** – Application runtime
- **Discord.js** – Discord bot functionality
- **MongoDB** – Database and persistent storage
- **Groq API** – AI responses
- **dotenv** – Environment variable management

---

## Getting Started

Follow these steps to run BauaaCore locally.

### Requirements

Before starting, make sure you have:

- Node.js and npm installed
- A Discord application and bot token
- A MongoDB database
- A Groq API key

### 1. Clone the repository

```bash
git clone https://github.com/DhruvPatel011/BauaaCore.git
```

### 2. Open the project folder

```bash
cd BauaaCore
```

### 3. Install dependencies

```bash
npm install
```

### 4. Configure environment variables

Create a `.env` file in the root directory and add your credentials:

```env
DISCORD_TOKEN=your_discord_bot_token
MONGODB_URI=your_mongodb_connection_string
GROQ_API_KEY=your_groq_api_key
BOT_OWNER_ID=your_discord_user_id

PORT=10000
GROQ_MODEL=openai/gpt-oss-20b
```

Replace the example values with your actual credentials.

`PORT` and `GROQ_MODEL` are optional. The default port is `10000`, and the default model is `openai/gpt-oss-20b`.

### 5. Start the bot

```bash
npm start
```

Once configured correctly, BauaaCore will connect to Discord and initialize its services.

---

## Logging Channels

The default logging configuration uses the following channel names:

| Channel | Purpose |
|---|---|
| `all-logs` | General server logs |
| `kick-ban-logs` | Kick and ban events |
| `main-bots-logs` | Bot-related logs |
| `role-logs` | Role activity |
| `deleted-msg-logs` | Deleted messages |
| `edited-msg-logs` | Edited messages |
| `vc-logs` | Voice activity |
| `channel-logs` | Channel activity |
| `members-log` | Member activity |

Use `/setup-logs` to configure the logging channels.

---

## Health Endpoints

BauaaCore also provides HTTP endpoints for basic application monitoring.

| Endpoint | Purpose |
|---|---|
| `/` | Basic application response |
| `/health` | Application health check |
| `/ready` | Readiness check |

---

## Security

Keep your credentials safe.

- Never share your Discord bot token.
- Do not upload your `.env` file to GitHub.
- Keep your MongoDB connection string private.
- Never expose your Groq API key.

---

## License

This project is provided under the **BauaaCore Educational Use License**.

Please read the [LICENSE](LICENSE) file before using, modifying, or distributing this project.

---

## Author

**Bauaa**

GitHub: [@DhruvPatel011](https://github.com/DhruvPatel011)

Repository: [BauaaCore](https://github.com/DhruvPatel011/BauaaCore)

