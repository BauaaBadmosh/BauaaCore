# BauaaCore

\<p align="center">
&#x20; \<img src="assets/BauaaCore%20Dragon%20Wordmark.png" alt="BauaaCore – Discord Bot" width="850">
\</p>

\<p align="center">
&#x20; A Discord bot for server activity logging, moderation visibility, and AI-powered conversations.
\</p>

\<p align="center">
&#x20; \<img src="[https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white](https://img.shields.io/badge/Node.js-339933?style=flat\&logo=node.js\&logoColor=white)" alt="Node.js">
&#x20; \<img src="[https://img.shields.io/badge/Discord.js-v14-5865F2?style=flat&logo=discord&logoColor=white](https://img.shields.io/badge/Discord.js-v14-5865F2?style=flat\&logo=discord\&logoColor=white)" alt="Discord.js">
&#x20; \<img src="[https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white](https://img.shields.io/badge/MongoDB-47A248?style=flat\&logo=mongodb\&logoColor=white)" alt="MongoDB">
&#x20; \<img src="[https://img.shields.io/badge/AI-Groq-F55036?style=flat](https://img.shields.io/badge/AI-Groq-F55036?style=flat)" alt="Groq AI">
&#x20; \<img src="[https://img.shields.io/badge/License-Educational%20Use-lightgrey?style=flat](https://img.shields.io/badge/License-Educational%20Use-lightgrey?style=flat)" alt="License">
\</p>

\<p align="center">
&#x20; \<a href="#about">About\</a> ·
&#x20; \<a href="#features">Features\</a> ·
&#x20; \<a href="#screenshots">Screenshots\</a> ·
&#x20; \<a href="#commands">Commands\</a> ·
&#x20; \<a href="#getting-started">Installation\</a>
\</p>

---

## About

BauaaCore is a Discord bot designed to make server management and activity monitoring easier.

It brings together server event logging, ignore management, and an AI assistant that can be configured for selected channels.

The bot uses Node.js and discord.js for Discord interactions, MongoDB for persistent configuration and AI memory, and Groq for AI-powered responses.

Built and maintained by **Bauaa**.

## Features

### Server Logging

Keep track of important activities happening across your Discord server.

- Member join and leave events
- Message deletion and editing
- Role creation, deletion, and updates
- Channel changes
- Voice channel join and leave activity
- Kick and ban events
- Bot-related activity

Logging events can be organized into dedicated channels, making server activity easier to review.

### Ignore Management

Control which entities should be excluded from logging.

- Ignore users
- Ignore bots
- Ignore webhooks
- Remove ignored entries
- View the ignore list

### AI Assistant

BauaaCore includes an AI assistant powered by the Groq API.

- Configure AI-enabled channels
- Enable or disable the assistant
- View the current AI status
- Change the assistant's mood
- Set custom AI instructions
- Reset conversation context

### AI Memory

The assistant supports user-specific memory stored in MongoDB.

- View saved memories
- Add new memories
- Forget individual memories
- Clear saved memories
- Memory expiry configured for 180 days

---

## Screenshots

A look at BauaaCore running inside Discord.

### Server Logging

Voice channel activity is displayed through organized Discord log messages.

\<p align="center">
&#x20; \<img src="assets/Screenshot%202026-11-17%20092314.png" alt="BauaaCore voice channel logging" width="100%">
\</p>

### Slash Commands

Access bot functionality directly through Discord's slash command interface.

\<p align="center">
&#x20; \<img src="assets/Screenshot%202026-11-17%20092426.png" alt="BauaaCore slash commands" width="100%">
\</p>

### AI Assistant

Interact with the AI assistant directly inside a configured Discord channel.

\<p align="center">
&#x20; \<img src="assets/Screenshot%202026-11-17%20092457.png" alt="BauaaCore AI assistant conversation" width="100%">
\</p>

### Bot Profile

\<p align="center">
&#x20; \<img src="assets/Screenshot%202026-11-17%20092543.png" alt="BauaaCore Discord bot profile" width="420">
\</p>

---

## Architecture

BauaaCore connects Discord events and commands with its bot services, database, and AI provider.

\<p align="center">
&#x20; \<img src="assets/BauaaCore%20System%20Architecture%20Flow\.png" alt="BauaaCore system architecture" width="100%">
\</p>

The following visual provides another overview of the system's main components.

\<p align="center">
&#x20; \<img src="assets/BauaaCore%20System%20Flow%20Infographic.png" alt="BauaaCore system flow infographic" width="100%">
\</p>

### Main Components

| Component  | Responsibility                  |
| ---------- | ------------------------------- |
| Discord.js | Discord events and interactions |
| Node.js    | Application runtime             |
| MongoDB    | Configuration and AI memory     |
| Groq API   | AI response generation          |
| dotenv     | Environment configuration       |

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
| `/ignore remove` | Remove an entry from the ignore list           |
| `/ignore list`   | View ignored entries                           |

### AI Assistant

| Command              | Description                         |
| -------------------- | ----------------------------------- |
| `/ai-setup`          | Configure the AI assistant          |
| `/ai-add-channel`    | Add a channel where AI is available |
| `/ai-remove-channel` | Remove an AI-enabled channel        |
| `/ai-list-channels`  | View AI-enabled channels            |
| `/ai-enable`         | Enable the AI assistant             |
| `/ai-disable`        | Disable the AI assistant            |
| `/ai-status`         | Check AI status                     |
| `/ai-mood`           | Change the assistant's mood         |
| `/ai-reset`          | Reset conversation context          |

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

`PORT` and `GROQ_MODEL` are optional. The application uses `10000` and `openai/gpt-oss-20b` as their defaults.

**Keep your credentials private. Never upload your `.env` file to GitHub.**

### 5. Start the bot

```bash
npm start
```

The start script runs:

```bash
node src/index.js
```

Once configured correctly, BauaaCore will connect to Discord and initialize its services.

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

BauaaCore also provides HTTP endpoints for basic application monitoring.

| Endpoint  | Purpose                    |
| --------- | -------------------------- |
| `/`       | Basic application response |
| `/health` | Application health check   |
| `/ready`  | Readiness check            |

---

## Security

A few important practices when running BauaaCore:

- Never share your Discord bot token.
- Keep your MongoDB connection string private.
- Never expose your Groq API key.
- Do not upload `.env` files or credentials to GitHub.
- Grant the bot only the Discord permissions it needs.
- Configure the required Gateway Intents in the Discord Developer Portal.

---

## Project Structure

The main application is organized into the following directories:

```text
BauaaCore/
│
├── assets/
│   └── images and project visuals
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

Permission is limited to personal learning and non-commercial educational use, subject to the terms of the license.

Commercial use and redistribution require prior written permission from the copyright holder.

Read the [LICENSE](LICENSE) file before using or modifying the project.

---

## Author

\<p align="center">
&#x20; \<img src="assets/bauaa-logo.png" alt="Bauaa logo" width="100">
\</p>

\<p align="center">   \<strong>Bauaa\</strong>\<br>   Creator and Developer of BauaaCore \</p>

\<p align="center">   \<a href="[https://github.com/DhruvPatel011](https://github.com/DhruvPatel011)">GitHub Profile\</a> ·   \<a href="[https://github.com/DhruvPatel011/BauaaCore](https://github.com/DhruvPatel011/BauaaCore)">BauaaCore Repository\</a> \</p>

---

\<p align="center">   \<strong>BauaaCore\</strong>\<br>   Keeping Discord communities organized. \</p>
