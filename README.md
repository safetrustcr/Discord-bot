
# 🚀 Discord Bot - Setup and Usage Guide

Welcome to the **Discord Bot** setup guide! This document will walk you through everything you need to get this bot up and running, starting from creating a bot in the Discord Developer Portal to running the code on your machine.

---

## 📜 **Table of Contents**
1. 🛠 [Prerequisites](#prerequisites)
2. 🖥 [Create a Bot in Discord Developer Portal](#create-a-bot-in-discord-developer-portal)
3. 📂 [Clone the Repository](#clone-the-repository)
4. ⚙️ [Set Up the Environment](#set-up-the-environment)
5. 📝 [Configure `config.json`](#configure-configjson)
6. ▶️ [Run the Bot](#run-the-bot)
7. 🔍 [Additional Notes](#additional-notes)
8. ❓ [Troubleshooting](#troubleshooting)
9. 🤝 [How to Contribute](#how-to-contribute)

---

## 🛠 **Prerequisites**
Make sure you have the following installed on your machine:
- **Node.js** (version 16.9.0 or higher) ➡️ [Node.js Official Website](https://nodejs.org/)
- **Git** (to clone the repository) ➡️ [Git Official Website](https://git-scm.com/)
- **MongoDB** (to handle database operations) ➡️ [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)

---

## 🖥 **Create a Bot in Discord Developer Portal**
1. 🌐 Go to the [Discord Developer Portal](https://discord.com/developers/applications).
2. ➕ Click **"New Application"** and give your bot a name.
3. 🔧 Navigate to the **"Bot"** tab on the left menu and click **"Add Bot"**.
4. 🎨 Customize the bot profile (name, profile picture, etc., optional).
5. 🔑 Under the **Token** section, click **"Reset Token"** and copy the token.
   - ⚠️ **WARNING:** Do not share your token with anyone.

### **Enable Privileged Intents**
1. Navigate to the **"Bot"** tab and enable the following intents:
   - ✅ **Message Content Intent**
   - ✅ **Presence Intent**
   - ✅ **Server Members Intent**

### **Invite the Bot to Your Server**
1. Navigate to the **"OAuth2"** tab and go to **"URL Generator"**.
2. Select the following scopes:
   - `bot`
   - `applications.commands`
3. Under **Bot Permissions**, choose permissions your bot needs (e.g., Administrator or custom).
4. Copy the generated URL and open it in your browser.
5. Select your server and click **"Authorize"**.

---

## 📂 **Clone the Repository**
1. Open a terminal and run the following command:
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_BOT_REPO.git
   ```
2. Navigate into the project folder:
   ```bash
   cd YOUR_BOT_REPO
   ```

---

## ⚙️ **Set Up the Environment**

### **Install Dependencies**
1. Run the following command to install all required dependencies:
   ```bash
   npm install
   ```

---

## 📝 **Configure `config.json`**
1. Open the `config.json` file in the root directory.
2. Replace placeholders with your actual configuration:
   ```json
   {
       "token": "YOUR_DISCORD_BOT_TOKEN",
       "mongopass": "YOUR_MONGODB_CONNECTION_STRING",
       "clientId": "YOUR_CLIENT_ID",
       "guildId": "YOUR_GUILD_ID",

       "webhookIssue": "YOUR_ISSUE_WEBHOOK_URL",
       "webhookAntiCrash": "YOUR_ANTI_CRASH_WEBHOOK_URL",

       "roleIdBan": "YOUR_BAN_ROLE_ID",
       "roleIdClear": "YOUR_CLEAR_ROLE_ID",
       "roleIdCW": "YOUR_CW_ROLE_ID",
       "roleIdMute": "YOUR_MUTE_ROLE_ID",
       "roleIdWarn": "YOUR_WARN_ROLE_ID",
       "roleIdWarnings": "YOUR_WARNINGS_ROLE_ID",
       "roleIdAdmin": "YOUR_ADMIN_ROLE_ID",
       "roleDevId": "YOUR_DEVELOPER_ROLE_ID"
   }
   ```

### **Explanation of Fields**
- **token**: Your bot's token from the Developer Portal.
- **mongopass**: Your MongoDB connection string (e.g., MongoDB Atlas).
- **clientId**: The Client ID from the Developer Portal.
- **guildId**: The ID of the server where your bot is deployed.
- **webhookIssue**: Webhook URL for logging issues.
- **webhookAntiCrash**: Webhook URL for crash logs.
- **roleIdBan, roleIdClear, etc.**: Role IDs for specific functionalities.

---

## ▶️ **Run the Bot**
1. Start the bot by running:
   ```bash
   node .
   ```
2. If everything is set up correctly, you should see:
   ```
   BotName#1234 has started successfully.
   ```
3. Your bot is now online! 🎉

---

## 🔍 **Additional Notes**

### **Command Structure**
- **Commands**: Slash commands are located in the `Commands` folder.
- **Prefix Commands**: Prefix commands are in the `CommandsPrefix` folder.

### **Event Handlers**
- Events are located in the `Events` folder.

### **Database Configuration**
- Ensure your MongoDB database is running and accessible.

---

## ❓ **Troubleshooting**

### Bot Not Responding
- Check if the bot is online in your server.
- Verify the token in `config.json`.

### MongoDB Issues
- Ensure your MongoDB URI is correct and your database is accessible.

### Commands Not Working
- Ensure the bot has permissions to execute commands.
- Check if slash commands were correctly registered.

---

## 🤝 **How to Contribute**
1. Fork the repository to your GitHub account.
2. Clone your forked repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_FORKED_REPO.git
   ```
3. Create a new branch for your feature or bug fix:
   ```bash
   git checkout -b feature/your-feature-name
   ```
4. Make your changes and commit them:
   ```bash
   git add .
   git commit -m "Add your commit message here"
   ```
5. Push your changes to your forked repository:
   ```bash
   git push origin feature/your-feature-name
   ```
6. Open a pull request to the main repository.

### Contribution Guidelines
- Ensure your code follows the existing style and structure.
- Test your changes thoroughly before submitting a pull request.
- Include clear and concise commit messages.

---

## 💬 **Support**
- Open an issue in the GitHub repository.
- Join our support server (if available).
- Contact the developer listed in the `roleDevId` field of `config.json`.

---