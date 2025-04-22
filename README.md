### 🚀 Bot Setup Guide

Welcome to the bot setup guide! Follow the steps below to install and configure the bot correctly. This guide is designed for new users, with clear explanations for each step.

> 📱 **For Mobile Users (Termux):** [View the guide here](https://github.com/MeoMunDep/Guides-for-using-my-script-on-termux)

---

## 📌 Table of Contents

1. [System Requirements](#system-requirements)
2. [Installing the Bot](#installing-the-bot)
   - [Install via Git](#install-via-git)
   - [Manual Installation](#manual-installation)
   - [Install via Docker](#install-via-docker)
3. [Bot Configuration](#bot-configuration)
   - [`configs.json`](#1-configsjson)
   - [`datas.txt`](#2-datastxt)
   - [`proxies.txt`](#3-proxiestxt)
   - [`wallets.txt`](#4-walletstxt)
4. [Running the Bot](#running-the-bot)
5. [Updating the Bot](#updating-the-bot)
6. [Contact & Support](#contact-support)

---

## 📌 System Requirements

Before running the bot, make sure you have installed:

- **Node.js** (Version: `22.11.0`)
- **npm** (Version: `10.9.0`)
- **Git** (For downloading and updating the bot easily)
- **Docker** _(Optional: If you want to run the bot in a container)_

📥 **Download Node.js and npm here:** [Download Link](https://t.me/KeoAirDropFreeNe/257/1462).
📥 **Download Git here:** [Download Link](https://t.me/KeoAirDropFreeNe/257/60831).

---

## 📌 Installing the Bot

### 🔹 Install via Git

1. **Download the bot**:
   ```bash
   git clone https://github.com/MeoMunDep/Tomo-wallet.git
   cd TomoWallet/TomoWallet
   ```
2. **Install required libraries**:
   ```bash
   npm install --force user-agents axios colors https-proxy-agent socks-proxy-agent
   ```
3. **Prepare configuration files** ([See details](#bot-configuration))

### 🔹 Manual Installation (Without Git)

1. **Download and extract the bot** into a folder on your computer.
2. **Install required libraries** (same as Step 2 above).

### 🔹 Install via Docker

1. **Install Docker** if you haven’t already: [Docker Installation Guide](https://t.me/KeoAirDropFreeNe/257/60831).
2. **Build and run the bot using Docker**:
   ```bash
   docker build -t TomoWallet-image .
   docker run -d --name TomoWallet-container -v $(pwd)/logs:/app/logs TomoWallet-image
   ```
   **For Windows CMD:** Use `%cd%` instead of `$(pwd)`.

---

## 📌 Bot Configuration

### 1. `configs.json` - 📜 Main Configuration

```json
{
  "rotateProxy": false,
  "skipInvalidProxy": false,
  "proxyRotationInterval": 2,
  "delayEachAccount": [5, 8],
  "timeToRestartAllAccounts": 300,
  "howManyAccountsRunInOneTime": 100,
  "doTasks": true
}
```

Explanation of each parameter:

| **Parameter Name**            | **Data Type**      | **Default Value** | **Description**                                                                   |
| ----------------------------- | ------------------ | ----------------- | --------------------------------------------------------------------------------- |
| `rotateProxy`                 | `boolean`          | `false`           | Enable/disable automatic proxy rotation between accounts.                         |
| `skipInvalidProxy`            | `boolean`          | `false`           | If `true`, the bot will skip that account due to invalid proxy.                   |
| `proxyRotationInterval`       | `number`           | `2`               | Time interval (in minutes) between proxy rotations when `rotateProxy` is enabled. |
| `delayEachAccount`            | `[number, number]` | `[5, 8]`          | Random delay (in seconds) between accounts when performing tasks.                 |
| `timeToRestartAllAccounts`    | `number`           | `300`             | Time (in seconds) before the bot restarts all accounts.                           |
| `howManyAccountsRunInOneTime` | `number`           | `100`             | Number of accounts running simultaneously.                                        |
| `doTasks`                     | `boolean`          | `true`            | Enable/disable task execution (`false` means the bot won’t perform tasks).        |

### 2. `datas.txt` - 🗂️ User Data

- [Get it from here](https://t.me/KeoAirDropFreeNee/1586)

```txt
query_id.../user...
query_id.../user...
query_id.../user...
```

### 3. `proxies.txt` - 🌐 Proxy (Optional)

- [Get it from here](https://www.webshare.io/?referral_code=4l5kb3glsce7)

```txt
http://host:port
https://host:port
socks4://host:port
socks5://host:port
http://user:pass@host:port
https://user:pass@host:port
socks4://user:pass@host:port
socks5://user:pass@host:port
```

### 4. `wallets.txt` - 💼 Wallet List

- [Get it from here](https://github.com/MeoMunDep/Automatic-Ultimate-Create-Wallets-for-Airdrop)

```txt
abc...xyz
abc...xyz
abc...xyz
```

---

## 📌 Running the Bot

### **Run on PC:**

```bash
node meomundep.js
```

### **Run with batch script on Windows:**

1. Open **Command Prompt (CMD)**.
2. Navigate to the bot folder:
   ```cmd
   cd "path\to\TomoWallet"
   ```
3. Run the batch script:
   ```cmd
   run.bat
   ```
   _(\*If you encounter permission issues, right-click `run.bat` and select "Run as Administrator".)_

### **Run with shell script on Linux/macOS:**

```bash
./run.sh
```

### **Run using Docker:**

```bash
docker start TomoWallet-container
```

---

## 📌 Updating the Bot

### 🔹 If installed via Git

```bash
cd TomoWallet
git pull origin main
npm install
```

### 🔹 If running via Docker

```bash
docker stop TomoWallet-container
docker rm TomoWallet-container
docker build -t TomoWallet-image .
docker run -d --name TomoWallet-container TomoWallet-image
```

---

## 📌 Contact & Support

- **Support me via** [Referral Link](https://t.me/tomowalletbot/tomo_wallet_app?startapp=VA426WC6LK)
- **Support me via Donate** [Here](https://t.me/KeoAirDropFreeNe/312/27801)
- **Contact for work:** [Telegram](https://t.me/MeoMunDep)
- **Join the support group:** [Join here](https://t.me/KeoAirDropFreeNe)
- **Updates Channel:** [View channel](https://t.me/KeoAirDropFreeNee)
- **YouTube Channel:** [Watch here](https://www.youtube.com/@keoairdropfreene)
- **Instagram:** [Follow me](https://www.instagram.com/meomundep)
- **Tiktok:** [Follow me](https://www.tiktok.com/@meomundep)

⚠️ **Disclaimer**: This code is provided "as is" without any warranties. Use it at your own risk. You are solely responsible for any consequences arising from its use. Redistribution or sale of this code in any form is strictly prohibited.
✨ Thank you for using the bot! Good luck! 🚀
