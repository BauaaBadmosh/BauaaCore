# 🚀 BauaaCore

\<p align="center">
&#x20; \<strong>A Powerful Discord Bot for Server Management, Logging & AI-Powered Conversations.\</strong>
\</p>

\<p align="center">
&#x20; \<img src="[https://img.shields.io/badge/Node.js-18%2B-339933?style=for-the-badge&logo=node.js&logoColor=white](https://img.shields.io/badge/Node.js-18%2B-339933?style=for-the-badge\&logo=node.js\&logoColor=white)" alt="Node.js" />
&#x20; \<img src="[https://img.shields.io/badge/Discord.js-14-5865F2?style=for-the-badge&logo=discord&logoColor=white](https://img.shields.io/badge/Discord.js-14-5865F2?style=for-the-badge\&logo=discord\&logoColor=white)" alt="Discord.js" />
&#x20; \<img src="[https://img.shields.io/badge/Database-MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white](https://img.shields.io/badge/Database-MongoDB-47A248?style=for-the-badge\&logo=mongodb\&logoColor=white)" alt="MongoDB" />
&#x20; \<img src="[https://img.shields.io/badge/AI-Groq-orange?style=for-the-badge](https://img.shields.io/badge/AI-Groq-orange?style=for-the-badge)" alt="Groq AI" />
\</p>

\<p align="center">
&#x20; \<a href="#-features">Features\</a> •
&#x20; \<a href="#-commands">Commands\</a> •
&#x20; \<a href="#-installation">Installation\</a> •
&#x20; \<a href="#-configuration">Configuration\</a> •
&#x20; \<a href="#-license">License\</a>
\</p>

---

## ✨ Overview

**BauaaCore** is a multifunctional Discord bot designed to simplify server management, automate moderation logging, and bring AI-powered conversations directly into your Discord community.

Built with Node.js and Discord.js, it combines server activity tracking, customizable logging, ignore management, and AI interactions with persistent memory.

## 🌟 Features

| Feature                   | Description                                               |
| ------------------------- | --------------------------------------------------------- |
| 📋 Advanced Logging       | Track server events and activities in dedicated channels. |
| 🛡️ Moderation Logs       | Monitor kick and ban activities.                          |
| 👥 Member Logs            | Track member-related events.                              |
| 💬 Message Logs           | Monitor deleted and edited messages.                      |
| 🎭 Role Logs              | Track role creation, deletion and updates.                |
| 🔊 Voice Logs             | Monitor voice channel activities.                         |
| 🚫 Ignore System          | Exclude selected users, bots and webhooks from logging.   |
| 🤖 AI Assistant           | Enable AI-powered conversations in selected channels.     |
| 🧠 Persistent AI Memory   | Maintain user-specific conversational memory.             |
| ⚙️ Custom AI Instructions | Configure AI behavior and personality.                    |
| ❤️ Health Endpoints       | Monitor application health and readiness.                 |

## 🧩 Logging System

BauaaCore organizes server activity into dedicated logging channels.

**Default logging channels:**

- `all-logs`
- `kick-ban-logs`
- `main-bots-logs`
- `role-logs`
- `deleted-msg-logs`
- `edited-msg-logs`
- `vc-logs`
- `channel-logs`
- `members-log`

Use `/setup-logs` to configure the logging system.

## 🤖 AI Assistant

BauaaCore includes an AI assistant powered by Groq.

**AI capabilities:**

- AI conversations in configured channels.
- Enable or disable AI functionality.
- Configure AI personality and instructions.
- User-specific memory stored in MongoDB.
- Manage, add, list and clear saved memories.
- Reset conversational context.

## ⚡ Commands

### Logging & Ignore Commands

| Command          | Description                        |
| ---------------- | ---------------------------------- |
| `/setup-logs`    | Configure server logging channels. |
| `/ignore add`    | Ignore a user, bot or webhook.     |
| `/ignore remove` | Remove an ignored entity.          |
| `/ignore list`   | Display ignored entities.          |

### AI Commands

| Command              | Description                    |
| -------------------- | ------------------------------ |
| `/ai-setup`          | Set up AI functionality.       |
| `/ai-add-channel`    | Add an AI-enabled channel.     |
| `/ai-remove-channel` | Remove an AI-enabled channel.  |
| `/ai-list-channels`  | List configured AI channels.   |
| `/ai-enable`         | Enable the AI assistant.       |
| `/ai-disable`        | Disable the AI assistant.      |
| `/ai-status`         | Check AI status.               |
| `/ai-mood`           | Configure AI mood.             |
| `/ai-reset`          | Reset AI conversation context. |

### AI Memory Commands

| Command             | Description           |
| ------------------- | --------------------- |
| `/ai-memory list`   | View saved memories.  |
| `/ai-memory add`    | Add a memory.         |
| `/ai-memory forget` | Forget a memory.      |
| `/ai-memory clear`  | Clear saved memories. |

### AI Instructions

| Command                  | Description                |
| ------------------------ | -------------------------- |
| `/ai-instructions view`  | View current instructions. |
| `/ai-instructions set`   | Set custom instructions.   |
| `/ai-instructions clear` | Clear custom instructions. |

## 🛠️ Technology Stack

| Technology | Purpose                   |
| ---------- | ------------------------- |
| Node.js    | Runtime environment       |
| Discord.js | Discord API integration   |
| MongoDB    | Persistent data storage   |
| Groq API   | AI-powered conversations  |
| dotenv     | Environment configuration |

## 📦 Installation

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

Create a `.env` file in the project root:

```env
DISCORD_TOKEN=your_discord_bot_token
MONGODB_URI=your_mongodb_connection_string
GROQ_API_KEY=your_groq_api_key
BOT_OWNER_ID=your_discord_user_id

PORT=10000
GROQ_MODEL=openai/gpt-oss-20b
```

### 5. Start the bot

```bash
npm start
```

## ⚙️ Configuration

Before starting BauaaCore, make sure you have:

- A Discord application and bot token.
- Required Discord Gateway Intents enabled.
- A MongoDB connection string.
- A Groq API key.
- Your Discord user ID for bot-owner configuration.

**Environment variables:**

| Variable        | Required | Description                            |
| --------------- | -------- | -------------------------------------- |
| `DISCORD_TOKEN` | Yes      | Discord bot token                      |
| `MONGODB_URI`   | Yes      | MongoDB connection string              |
| `GROQ_API_KEY`  | Yes      | Groq API key                           |
| `BOT_OWNER_ID`  | Yes      | Bot owner's Discord ID                 |
| `PORT`          | No       | HTTP server port; default `10000`      |
| `GROQ_MODEL`    | No       | AI model; default `openai/gpt-oss-20b` |

> Never upload your `.env` file or expose your API keys publicly.

## ❤️ Health Monitoring

BauaaCore provides HTTP endpoints for application monitoring.

| Endpoint  | Purpose                    |
| --------- | -------------------------- |
| `/`       | Basic application response |
| `/health` | Health check               |
| `/ready`  | Readiness check            |

## 📁 Project Structure

```text
BauaaCore/
├── src/
│   ├── config/
│   │   └── logs.js
│   ├── commands/
│   ├── events/
│   ├── utils/
│   └── index.js
├── package.json
├── package-lock.json
├── .env.example
├── .gitignore
├── README.md
└── LICENSE
```

*The directory listing above is a simplified overview; actual folders may vary.*

## 🔐 Security

- Keep bot tokens and API keys private.
- Use environment variables for sensitive configuration.
- Never commit your `.env` file.
- Restrict access to your MongoDB database.

## 📄 License

BauaaCore is distributed under the **BauaaCore Educational Use License**.

It is intended for educational and personal learning purposes, subject to the conditions in the [LICENSE](LICENSE) file.

## 👨‍💻 Author

**Created with ❤️ by Bauaa**

\<p align="center">   \<strong>BauaaCore\</strong>\<br/>   Built to make Discord server management smarter. \</p>

\<p align="center">   \<a href="[https://github.com/DhruvPatel011/BauaaCore](https://github.com/DhruvPatel011/BauaaCore)">GitHub Repository\</a> \</p>
