# 🤖 Self Nix — Command Reference

> Complete documentation for the public commands and user-facing features of Self Nix.

---

## 📚 Table of Contents

- 🚀 [Getting Started](#-getting-started)
  - [`/start`](#start)
  - [`/help`](#help)
- 👤 [Account](#-account)
  - [`/level`](#level)
  - [`/profile`](#profile)
  - [`/balance`](#balance)
  - [`/transfer`](#transfer)
- 🪙 [Nix Coin](#-nix-coin)
- 🎮 [Games](#-games)
  - [Dōz 20](#-dōz-20)
  - [Sangchi 20](#-sangchi-20)
  - [Mine Rub 20](#-mine-rub-20)
  - [Bāzi 20](#-bāzi-20)
- 🏆 [Statistics](#-statistics)
  - [Coin Ranking](#coin-ranking)
  - [Win Ranking](#win-ranking)
- 🔐 [Administration](#-administration)

---

# 🚀 Getting Started

## `/start`

Starts the Self Nix interface and opens the main user panel.

The main panel provides access to the core Self Nix services.

### Available Features

- 🔐 Self activation
- 🪙 Nix Coin purchase
- 🌐 Subscription services
- ⚙️ Self management
- 👤 Account information
- 🔗 Referral system
- 🧪 One-day trial
- 💬 Support and contact options

### Usage

```text
/start

Availability

«"/start" is intended for private chat.»

---

"/help"

Opens the Self Nix help center.

The help system provides information about the available features and user systems.

Help Sections

- 📖 Command Guide
- 🔐 Self Activation Guide
- 🏆 Level System
- 🪙 Nix Coin System
- 🎁 Rewards
- 🎮 Game System
- ⚙️ General Features

Usage

/help

---

👤 Account

"/level"

Displays the user's current Level, XP, progression, rewards, and account statistics.

Level Information

The Level panel displays information such as:

Field| Description
🏅 Level| Current user Level
⭐ XP| Current experience points
⬆️ Next Level| XP required to reach the next Level
🎁 Next Reward| Reward available at the next Level
📊 Progress| Current Level progression

Account Statistics

The Level panel can also display:

- 💳 Registered transaction volume
- 🪙 Purchased Nix Coins
- 💵 Total amount spent on Coins
- 💰 Wallet deposits
- 🔐 Number of configurations
- 📦 Configuration traffic
- ♻️ Renewals
- 👥 Successful referrals
- 🎮 Recorded games
- 🪙 Current Nix Coin balance
- 💼 Wallet balance

Rewards

Users can view the rewards associated with their Levels.

The panel also displays previously received rewards when available.

Example

╭───────────────╮
🏆 Level 𝐋u𝐜𝐲 22:37
╰───────────────╯

🏅 Level: 1
⭐ XP: 0

⬆️ تا Level 2: 500 XP
🎁 جایزه بعدی: 🪙 10 سکه
▱▱▱▱▱▱▱▱▱▱ 0%

━━━━━━━━━━━━━━━━
📊 آمار حساب

💳 گردش مالی ثبت‌شده: 0 تومان
🪙 سکه خریداری‌شده: 0
💵 مبلغ خرید سکه: 0 تومان
💰 شارژ کیف پول: 0 تومان
🔐 تعداد کانفیگ: 0
📦 حجم کانفیگ: 0 GB
♻️ تمدید: 0
👥 دعوت موفق: 0
🎮 بازی ثبت‌شده: 0
🪙 موجودی سکه: 0
💼 کیف پول: 0 تومان

🎁 جوایز دریافت‌شده
هنوز جایزه‌ای دریافت نشده

---

"/profile"

Displays the user's Telegram and Self Nix account information.

Information

Depending on the available account data, the profile may include:

- 👤 Name
- 🆔 Telegram ID
- 🔗 Username
- 🖼️ Profile picture
- 📊 Self Nix account information

Usage

/profile

---

"/balance"

Displays the user's current Nix Coin balance.

The system can also display the approximate Toman value of the user's current Coin balance.

Example

🪙 Nix Coins: 500
💰 Approximate Value: 42,000 Toman

Usage

/balance

---

"/transfer"

Transfers Nix Coins from one Self Nix user to another.

Usage

/transfer {ID | Username | Reply} {Amount}

Recipient Methods

The recipient can be selected using:

- 🆔 Telegram ID
- 👤 Username
- 💬 Reply to the recipient's message

Transfer Fee

A 10% transaction fee is applied to Coin transfers.

Example

/transfer @username 11

Example Result

💸 انتقال سکه انجام شد

👤 دریافت کننده: کاربر
📤 مبلغ ارسال: 11
💳 کارمزد: 1
📥 مبلغ دریافتی: 10
♾️ موجودی شما: نامحدود
📅 تاریخ: 2026-09-25 16:47:15

---

🪙 Nix Coin

Nix Coin is the internal currency used throughout Self Nix.

Coin Balance

Displays the user's current Nix Coin balance.

The system can also show the approximate monetary value of the balance.

Coin Statistics

Provides Coin-related statistics and rankings.

Coin Transfer

Allows users to transfer Nix Coins between Self Nix accounts.

Transfer Fee

10%

---

🎮 Games

Self Nix includes multiplayer games where Nix Coins can be used as wagers.

Unless otherwise specified, the games in this section are designed for two players.

---

🟦 Dōz 20

A two-player Tic-Tac-Toe style game.

Players place their symbols on the board and attempt to create a line of three matching symbols.

Game Information

Property| Value
👥 Players| 2
🪙 Wager| 20 Nix Coins
🎯 Objective| Create a line of three

---

✂️ Sangchi 20

A two-player Rock-Paper-Scissors game.

Players choose between:

- 🪨 Rock
- 📄 Paper
- ✂️ Scissors

Match Modes

Players can choose the number of rounds:

1 Round
3 Rounds
5 Rounds

The player who wins the greater number of rounds wins the match.

Game Information

Property| Value
👥 Players| 2
🪙 Wager| 20 Nix Coins
🔄 Rounds| 1 / 3 / 5

---

💣 Mine Rub 20

A two-player hidden-mine game.

The game generates a hidden board containing 11 mines.

Players reveal hidden positions and attempt to find mines.

Finding a mine provides another opportunity to continue playing.

The player with the better final result wins the match.

Game Information

Property| Value
👥 Players| 2
🪙 Wager| 20 Nix Coins
💣 Mines| 11

---

🎮 Bāzi 20

A two-player automated game.

No special gameplay action is required from the players.

Once the second player joins the match, Self Nix automatically determines the winner.

Game Information

Property| Value
👥 Players| 2
🪙 Wager| 20 Nix Coins
🤖 Winner Selection| Automated

---

🏆 Statistics

🪙 Coin Ranking

Displays the Top 10 users with the highest Nix Coin balance.

Ranking

1. User
2. User
3. User
...
10. User

The ranking is based on the users' current Coin holdings.

---

🏆 Win Ranking

Displays the Top 10 users with the highest number of recorded game wins.

Ranking

1. User
2. User
3. User
...
10. User

---

🔐 Administration

«Administrative commands are intentionally not included in the current public command reference.»

The Administration section will be expanded in a future documentation update with the appropriate Admin and Owner commands and permission requirements.

---

🔒 Privacy & Source Code

This repository contains public documentation, examples, and information about the Self Nix service.

The following are not included:

- 🔒 Production source code
- 🔑 Bot tokens
- 🔐 Private credentials
- 🗄️ Database credentials
- ⚙️ Private production configuration
- 🧩 Internal implementation details
- 🛡️ Private security mechanisms

«Self Nix is proprietary software.»

This repository is intended to document and introduce the public-facing functionality of Self Nix without exposing its private implementation.
