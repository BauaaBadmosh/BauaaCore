# BauaaCore

![BauaaCore Banner](assets/BauaaCore%20Dragon%20Wordmark.png)

**A Discord bot for server activity logging, moderation visibility, and AI-powered conversations.**

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)
![Discord.js](https://img.shields.io/badge/Discord.js-v14-5865F2?style=flat&logo=discord&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![Groq AI](https://img.shields.io/badge/AI-Groq-F55036?style=flat)
![Educational License](https://img.shields.io/badge/License-Educational%20Use-lightgrey?style=flat)

[About](#about) · [Features](#features) · [Screenshots](#screenshots) · [Architecture](#architecture) · [Commands](#commands) · [Installation](#getting-started)

---

## About

BauaaCore is a Discord bot developed to make server management and activity monitoring easier.

It combines server event logging, ignore management, and an AI assistant that can be configured for selected channels.

Built using Node.js, discord.js, MongoDB, and the Groq API.

**Created and maintained by Bauaa.**

## Features

### Server Logging

Monitor important activities across your Discord server.

- Member join and leave events
- Message deletion and editing
- Role creation, deletion, and updates
- Channel changes
- Voice channel join and leave activity
- Kick and ban events
- Bot-related activity

### Ignore Management

Choose which entities should be excluded from logging.

- Ignore users
- Ignore bots
- Ignore webhooks
- Remove ignored entries
- View the ignore list

### AI Assistant

An AI assistant powered by Groq, available in configured Discord channels.

- Configure AI-enabled channels
- Enable or disable the assistant
- Check AI status
- Change the assistant's mood
- Set custom AI instructions
- Reset conversation context

### AI Memory

Store and manage user-specific conversational memories using MongoDB.

- View saved memories
- Add new memories
- Forget individual memories
- Clear saved memories
- Configured memory expiry: 180 days

---

## Screenshots

### Server Logging

BauaaCore records voice channel activity and displays it in Discord log messages.

![BauaaCore Logging Screenshot](assets/Screenshot%202026-11-17%20092314.png)

### Slash Commands

Access BauaaCore features directly using Discord slash commands.

![BauaaCore Commands Screenshot](assets/Screenshot%202026-11-17%20092426.png)

### AI Assistant

Interact with the AI assistant inside a configured Discord channel.

![BauaaCore AI Assistant Screenshot](assets/Screenshot%202026-11-17%20092457.png)

### Bot Profile

The BauaaCore bot profile and its Discord identity.

![BauaaCore Bot Profile](assets/Screenshot%202026-11-17%20092543.png)

### Additional Discord View

Another view of BauaaCore running inside Discord.

![BauaaCore Discord View](assets/Screenshot%202026-11-17%20092904.png)

---

## Architecture

The following diagram illustrates the main components of BauaaCore and how Discord, the bot application, MongoDB, and Groq AI interact.

![BauaaCore System Architecture](assets/BauaaCore%20System%20Architecture%20Flow.png)

### System Overview

![BauaaCore System Flow Infographic](assets/BauaaCore%20System%20Flow%20Infographic.png)

### Main Components

| Component | Purpose |
|---|---|
| Node.js | Application runtime |
| discord.js | Discord events and interactions |
| MongoDB | Persistent configuration and AI memory |
| Groq API | AI response generation |
| dotenv | Environment configuration |

---

## Commands

BauaaCore uses Discord slash commands.

### Logging

| Command | Description |
|---|---|
| `/setup-logs` | Configure server logging channels |

### Ignore Management

| Command | Description |
|---|---|
| `/ignore add` | Add a user, bot, or webhook to the ignore list |
| `/ignore remove` | Remove an ignored entry |
| `/ignore list` | View ignored entries |

### AI Assistant

| Command | Description |
|---|---|
| `/ai-setup` | Configure the AI assistant |
| `/ai-add-channel` | Add an AI-enabled channel |
| `/ai-remove-channel` | Remove an AI-enabled channel |
| `/ai-list-channels` | List AI-enabled channels |
| `/ai-enable` | Enable the AI assistant |
| `/ai-disable` | Disable the AI assistant |
| `/ai-status` | Check AI status |
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

## Getting Started

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

The default logging configuration uses these channel names:

| Channel | Purpose |
|---|---|
| `all-logs` | General server logs |
| `kick-ban-logs` | Kick and ban events |
| `main-bots-logs` | Bot-related activity |
| `role-logs` | Role activity |
| `deleted-msg-logs` | Deleted messages |
| `edited-msg-logs` | Edited messages |
| `vc-logs` | Voice channel activity |
| `channel-logs` | Channel activity |
| `members-log` | Member activity |

Use `/setup-logs` to configure logging channels for your server.

---

## Health Endpoints

BauaaCore exposes HTTP endpoints for basic application monitoring.

| Endpoint | Purpose |
|---|---|
| `/` | Basic application response |
| `/health` | Health check |
| `/ready` | Readiness check |

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

## Project Structure

```text
BauaaCore/
│
├── assets/
│   ├── bauaa-logo.png
│   ├── BauaaCore Dragon Wordmark.png
│   ├── BauaaCore System Architecture Flow.png
│   └── BauaaCore System Flow Infographic.png
│
├── src/
│   ├── ai/
│   ├── commands/
│   ├── config/
│   ├── events/
│   ├── utils/
│   └── index.js
│
├── tests/
├── package.json
├── .env.example
├── .gitignore
├── README.md
└── LICENSE
```

---

## License

BauaaCore is provided under the **BauaaCore Educational Use License**.

Permission is limited to personal learning and non-commercial educational use, subject to the terms in the license.

Commercial use and redistribution require prior written permission from the copyright holder.

See [LICENSE](LICENSE) for the complete terms.

---

## Author

![Bauaa Logo](assets/bauaa-logo.png)

**Bauaa**

Creator and Developer of BauaaCore.

[GitHub Profile](https://github.com/DhruvPatel011) · [BauaaCore Repository](https://github.com/DhruvPatel011/BauaaCore)

---

**BauaaCore** — Keeping Discord communities organized.
