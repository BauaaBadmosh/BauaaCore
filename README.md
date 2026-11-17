# BauaaCore

<img src="assets/bauaa-logo.png" width="80" align="left" alt="Bauaa Logo">
<img src="assets/BauaaCore%20Dragon%20Wordmark.png" height="90" alt="BauaaCore Dragon Wordmark">

<br clear="left">

**A Discord bot for server activity logging, moderation visibility, and AI-powered conversations.**

![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)
![Discord.js](https://img.shields.io/badge/Discord.js-v14-5865F2?style=flat&logo=discord&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![Groq AI](https://img.shields.io/badge/AI-Groq-F55036?style=flat)
![License](https://img.shields.io/badge/License-Educational%20Use-lightgrey?style=flat)

[About](#about) · [Features](#features) · [Screenshots](#screenshots) · [Architecture](#architecture) · [Commands](#commands) · [Installation](#getting-started)

---

## About

BauaaCore is a Discord bot developed to make server management and activity monitoring easier.

It brings together three main capabilities:

- **Server Logging** — Monitor important activities across your Discord server.
- **Ignore Management** — Exclude selected users, bots, or webhooks from logging.
- **AI Assistant** — Enable AI-powered conversations in configured channels.

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

Logs are organized into dedicated Discord channels to make server activity easier to review.

### Ignore Management

Choose which entities should be excluded from logging.

- Add users, bots, or webhooks to the ignore list
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

A look at BauaaCore running inside Discord.

### Server Logging

Monitor voice channel activity through structured Discord log messages.

<img src="assets/Screenshot%202026-11-17%20092314.png" width="100%" alt="BauaaCore Server Logging">

### AI Assistant

Interact with the AI assistant inside a configured Discord channel.

<img src="assets/Screenshot%202026-11-17%20092457.png" width="100%" alt="BauaaCore AI Assistant">

### Bot Profile

The BauaaCore bot profile and its Discord identity.

<img src="assets/Screenshot%202026-11-17%20092543.png" width="35%" alt="BauaaCore Bot Profile">

### Additional Discord View

Another view of BauaaCore running inside Discord.

<img src="assets/Screenshot%202026-11-17%20092904.png" width="100%" alt="BauaaCore Discord View">

---

## Architecture

BauaaCore connects Discord events and commands with its application services, database, and AI provider.

### System Architecture

<img src="assets/BauaaCore%20System%20Architecture%20Flow.png" width="100%" alt="BauaaCore System Architecture">

### System Overview

<img src="assets/BauaaCore%20System%20Flow%20Infographic.png" width="100%" alt="BauaaCore System Flow">

### Main Components

| Component | Responsibility |
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
| `/ai-instructions view` | View current AI instructions |
| `/ai-instructions set` | Set custom AI instructions |
| `/ai-instructions clear` | Clear custom AI instructions |

### Command Interface

Access BauaaCore features directly through Discord's slash command interface.

<img src="assets/Screenshot%202026-11-17%20092426.png" width="100%" alt="BauaaCore Slash Commands">

---

## Technology Stack

| Technology | Purpose |
|---|---|
| Node.js | JavaScript runtime |
| discord.js | Discord bot development |
| MongoDB | Database and persistent memory |
| Groq API | AI integration |
| dotenv | Environment variable management |

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
