# 🤖 Self Nix — Commands

**🌐 Language / زبان:** [فارسی](#-راهنمای-دستورات-فارسی) · [English](#-command-guide-english)

---

<a id="-راهنمای-دستورات-فارسی"></a>
# 📘 راهنمای دستورات (فارسی)

مستندات کامل دستورات ربات Self Nix — شامل دستورات حساب کاربری، سکه‌ها، بازی‌ها و رتبه‌بندی‌ها.

## 📚 فهرست مطالب

- [شروع کار](#-شروع-کار)
- [ساختار دستورات](#-ساختار-دستورات)
- [دستورات حساب کاربری](#-دستورات-حساب-کاربری)
- [نیکس کوین](#-نیکس-کوین)
- [بازی‌ها](#-بازیها)
- [آمار و رتبه‌بندی](#-آمار-و-رتبهبندی)
- [مدیریت](#-مدیریت)
- [خطاهای رایج](#️-خطاهای-رایج)
- [نکات مهم](#-نکات-مهم)
- [جدول مرجع سریع](#-جدول-مرجع-سریع)

---

## 🚀 شروع کار

هر دستور را می‌توان به سه شکل اجرا کرد:

- **فارسی** — مثال: `موجودی`
- **English** — مثال: `balance`
- **Slash Command** — مثال: `/balance`

هر سه روش عملکرد یکسانی دارند و بسته به ترجیح کاربر قابل استفاده‌اند.

---

## 📖 ساختار دستورات

### بدون پارامتر
```text
<command>
```
مثال:
```text
balance
/balance
```

### یک پارامتر
```text
<command> <parameter>
```

### چند پارامتر
```text
<command> <parameter_1> <parameter_2>
```
مثال واقعی:
```text
transfer 123 50
/transfer 123 50
```

| نماد | توضیح |
|---|---|
| `<user>` | کاربر مقصد (بر اساس ID، Username یا Reply) |
| `<amount>` | مقدار عددی (Nix Coin) |
| `<parameter>` | مقدار جایگزین‌شدنی |
| `/` | پیشوند Slash Command |
| `@username` | ارجاع به کاربر با نام کاربری |

**قوانین مهم Syntax:**
- علائم `< >` بخشی از Placeholder هستند و نباید عیناً وارد شوند.
- ترتیب پارامترها مهم است و نباید جابه‌جا شود.
- بین Command و هر Parameter باید فاصله وجود داشته باشد.
- مقادیر عددی باید عدد معتبر باشند.
- `@username` فقط در دستوراتی که از آن پشتیبانی می‌کنند قابل استفاده است.
- Reply فقط در مواردی که مستند شده پشتیبانی می‌شود (مانند `transfer`).

---

## 👤 دستورات حساب کاربری

### 1. 💰 موجودی / Balance

| | |
|---|---|
| فارسی | `موجودی` |
| English | `balance` |
| Slash | `/balance` |
| کاربرد | نمایش موجودی فعلی Nix Coin |
| Syntax | `balance` |
| Parameters | ندارد |

### 2. 👤 پروفایل / Profile

| | |
|---|---|
| فارسی | `پروفایل` |
| English | `profile` |
| Slash | `/profile` |
| کاربرد | نمایش اطلاعات حساب کاربری |
| Syntax | `profile` |
| Parameters | ندارد |

### 3. 💸 انتقال سکه / Transfer

| | |
|---|---|
| فارسی | `انتقال <user> <amount>` |
| English | `transfer <user> <amount>` |
| Slash | `/transfer <user> <amount>` |
| کاربرد | انتقال Nix Coin به کاربر دیگر |

**Parameters:**

| Parameter | Type | Description |
|---|---|---|
| `<user>` | User | کاربر دریافت‌کننده |
| `<amount>` | Number | مقدار Nix Coin برای انتقال |

کاربر مقصد می‌تواند بر اساس **ID**، **Username** یا در موارد پشتیبانی‌شده از طریق **Reply** مشخص شود.

**کارمزد انتقال:** `10%`

**Example Output:**
```text
💸 انتقال سکه انجام شد

👤 دریافت کننده: کاربر
📤 مبلغ ارسال: 11
💳 کارمزد: 1
📥 مبلغ دریافتی: 10
♾️ موجودی شما: نامحدود
📅 تاریخ: 2026-09-25 16:47:15
```

### 4. 🎛️ پنل / Panel

| | |
|---|---|
| فارسی | `پنل` |
| English | `panel` |
| Slash | `/panel` |
| کاربرد | دسترسی به پنل کاربری |
| Syntax | `panel` |
| Parameters | ندارد |

### 5. 🎁 روزانه / Daily

| | |
|---|---|
| فارسی | `روزانه` |
| English | `daily` |
| Slash | `/daily` |
| کاربرد | دریافت جایزه روزانه |
| Syntax | `daily` |
| Parameters | ندارد |

### 6. 🏅 سطح من / Level

| | |
|---|---|
| فارسی | `سطح من` |
| English | `level` |
| Slash | `/level` |
| کاربرد | نمایش سطح، XP و پیشرفت حساب |
| Syntax | `level` |
| Parameters | ندارد |

نمایش شامل:
- Level فعلی
- XP فعلی
- XP موردنیاز برای Level بعدی
- جایزه Level بعدی

در صورت نمایش، آمار حساب می‌تواند شامل موارد زیر باشد: گردش مالی، سکه خریداری‌شده، مبلغ خرید سکه، شارژ کیف پول، تعداد کانفیگ، حجم کانفیگ، تمدید، دعوت موفق، بازی ثبت‌شده، موجودی سکه، کیف پول.

**Example:**
```text
🏅 Level: 1
⭐ XP: 0

⬆️ تا Level 2: 500 XP
🎁 جایزه بعدی: 🪙 10 سکه
```

---

## 🪙 نیکس کوین

واحد پولی داخلی ربات که برای شارژ، ورود به بازی‌ها و انتقال بین کاربران استفاده می‌شود.

| Duration | Nix Coins |
|---|---|
| 1 Hour | 2 |
| 12 Hours | 24 |
| 24 Hours | 48 |
| 7 Days | 336 |
| 30 Days | 1440 |

---

## 🎮 بازی‌ها

### 🎯 دوز 20

| | |
|---|---|
| Players | 2 |
| Entry Cost | 20 Nix Coin |
| هدف | ساخت یک خط سه‌تایی (مشابه Tic-Tac-Toe) |

### ✊ سنگچی 20

| | |
|---|---|
| Players | 2 |
| Entry Cost | 20 Nix Coin |
| نوع | سنگ‌کاغذ‌قیچی (Rock-Paper-Scissors) |
| Rounds | 1 / 3 / 5 |

انتخاب حرکت از طریق Game Panel انجام می‌شود؛ بازیکنی که راند بیشتری ببرد برنده است.

### 💣 مین روب 20

| | |
|---|---|
| Players | 2 |
| Mines | 11 |
| Entry Cost | 20 Nix Coin |

بازیکنان مین‌ها را پیدا می‌کنند؛ هر مین پیدا‌شده می‌تواند فرصت ادامه بازی ایجاد کند. بازیکنی که مین بیشتری پیدا کند برنده است.

### 🎲 بازی 20

| | |
|---|---|
| Players | 2 |
| Entry Cost | 20 Nix Coin |

پس از ورود بازیکن دوم، سیستم به‌صورت خودکار برنده را مشخص می‌کند.

---

## 🏆 آمار و رتبه‌بندی

### 🪙 آمار سکه / Coin Leaderboard

| | |
|---|---|
| فارسی | `آمار سکه` |
| English | `leaderboard` |
| Slash | `/leaderboard` |
| کاربرد | نمایش Top 10 کاربران بر اساس Nix Coin |
| Parameters | ندارد |

### 🏆 آمار برد / Wins Leaderboard

| | |
|---|---|
| فارسی | `آمار برد` |
| English | `leaderboard_wins` |
| Slash | `/leaderboard_wins` |
| کاربرد | نمایش Top 10 کاربران بر اساس تعداد بردهای ثبت‌شده در بازی‌ها |
| Parameters | ندارد |

---

## 🔐 مدیریت

Coming Later

---

## ⚠️ خطاهای رایج

**Missing Required Parameters**
```text
transfer 123
```
Syntax صحیح:
```text
transfer 123 50
```

**Invalid Numeric Value**
```text
transfer 123 fifty
```

**Incorrect Parameter Order**
ترتیب صحیح باید مطابق `transfer <user> <amount>` باشد.

**Incorrect Spacing**
```text
transfer12350
```

**Literal Placeholders**
`transfer <user> <amount>` یک Syntax نمونه است و باید با مقادیر واقعی جایگزین شود.

---

## 💡 نکات مهم

- این فایل فقط مستندات عمومی ربات است.
- اطلاعات خصوصی (Token، API Key، Database و...) در این فایل قرار نمی‌گیرد.
- `<...>` باید همیشه با مقدار واقعی جایگزین شود.
- ترتیب پارامترها در تمام دستورات مهم است.
- قابلیت‌هایی که در این فایل مستند نشده‌اند، رسمی محسوب نمی‌شوند.
- بخش Administration فعلاً `Coming Later` است.

---

## 📋 جدول مرجع سریع

| Feature | فارسی | English | Slash |
|---|---|---|---|
| 💰 موجودی | موجودی | `balance` | `/balance` |
| 👤 پروفایل | پروفایل / حساب کاربری | `profile` | `/profile` |
| 💸 انتقال | انتقال | `transfer` | `/transfer` |
| 🎛️ پنل | پنل | `panel` | `/panel` |
| 🎁 روزانه | روزانه | `daily` | `/daily` |
| 🏅 سطح | سطح من | `level` | `/level` |
| 🪙 آمار سکه | آمار سکه | `leaderboard` | `/leaderboard` |
| 🏆 آمار برد | آمار برد | `leaderboard_wins` | `/leaderboard_wins` |

[⬆ Back to top / بازگشت به بالا](#-self-nix--commands)

---

<a id="-command-guide-english"></a>
# 📘 Command Guide (English)

Complete command documentation for the Self Nix bot — covering account commands, coins, games, and leaderboards.

## 📚 Table of Contents

- [Getting Started](#getting-started)
- [Command Syntax](#command-syntax)
- [Account Commands](#account-commands)
- [Nix Coin](#nix-coin)
- [Games](#games)
- [Statistics & Leaderboards](#statistics--leaderboards)
- [Administration](#administration)
- [Common Errors](#common-errors)
- [Notes](#notes)
- [Command Reference](#command-reference)

---

## Getting Started

Every command can be run in three equivalent forms:

- **Persian** — e.g. `موجودی`
- **English** — e.g. `balance`
- **Slash Command** — e.g. `/balance`

All three forms behave identically; use whichever fits your workflow.

---

## Command Syntax

### No parameters
```text
<command>
```
Example:
```text
balance
/balance
```

### One parameter
```text
<command> <parameter>
```

### Multiple parameters
```text
<command> <parameter_1> <parameter_2>
```
Real example:
```text
transfer 123 50
/transfer 123 50
```

| Symbol | Description |
|---|---|
| `<user>` | Target user (by ID, username, or reply) |
| `<amount>` | Numeric value (Nix Coin) |
| `<parameter>` | Generic placeholder value |
| `/` | Slash command prefix |
| `@username` | Reference a user by username |

**Key Syntax Rules:**
- `< >` marks a placeholder — do not type the angle brackets literally.
- Parameter order matters and must not be changed.
- A space is required between the command and each parameter.
- Numeric values must be valid numbers.
- `@username` only works on commands that explicitly support it.
- Reply is only supported where documented (e.g. `transfer`).

---

## Account Commands

### 1. 💰 Balance

| | |
|---|---|
| Persian | `موجودی` |
| English | `balance` |
| Slash | `/balance` |
| Purpose | Shows current Nix Coin balance |
| Syntax | `balance` |
| Parameters | None |

### 2. 👤 Profile

| | |
|---|---|
| Persian | `پروفایل` |
| English | `profile` |
| Slash | `/profile` |
| Purpose | Shows account information |
| Syntax | `profile` |
| Parameters | None |

### 3. 💸 Transfer

| | |
|---|---|
| Persian | `انتقال <user> <amount>` |
| English | `transfer <user> <amount>` |
| Slash | `/transfer <user> <amount>` |
| Purpose | Transfers Nix Coin to another user |

**Parameters:**

| Parameter | Type | Description |
|---|---|---|
| `<user>` | User | Recipient user |
| `<amount>` | Number | Amount of Nix Coin to transfer |

The recipient can be specified by **ID**, **username**, or, where supported, by **replying** to their message.

**Transfer fee:** `10%`

**Example Output:**
```text
💸 Transfer completed

👤 Recipient: user
📤 Amount sent: 11
💳 Fee: 1
📥 Amount received: 10
♾️ Your balance: Unlimited
📅 Date: 2026-09-25 16:47:15
```

### 4. 🎛️ Panel

| | |
|---|---|
| Persian | `پنل` |
| English | `panel` |
| Slash | `/panel` |
| Purpose | Access the user panel |
| Syntax | `panel` |
| Parameters | None |

### 5. 🎁 Daily

| | |
|---|---|
| Persian | `روزانه` |
| English | `daily` |
| Slash | `/daily` |
| Purpose | Claim the daily reward |
| Syntax | `daily` |
| Parameters | None |

### 6. 🏅 Level

| | |
|---|---|
| Persian | `سطح من` |
| English | `level` |
| Slash | `/level` |
| Purpose | Shows current level, XP, and progress |
| Syntax | `level` |
| Parameters | None |

Displayed information includes:
- Current level
- Current XP
- XP required for the next level
- Next level's reward

When shown, account statistics may include: financial turnover, coins purchased, coin purchase amount, wallet top-up, number of configs, config volume, renewals, successful referrals, recorded games, coin balance, wallet.

**Example:**
```text
🏅 Level: 1
⭐ XP: 0

⬆️ To Level 2: 500 XP
🎁 Next reward: 🪙 10 coins
```

---

## Nix Coin

The bot's internal currency, used for top-ups, joining games, and transfers between users.

| Duration | Nix Coins |
|---|---|
| 1 Hour | 2 |
| 12 Hours | 24 |
| 24 Hours | 48 |
| 7 Days | 336 |
| 30 Days | 1440 |

---

## Games

### 🎯 Tic-Tac-Toe 20

| | |
|---|---|
| Players | 2 |
| Entry Cost | 20 Nix Coin |
| Objective | Get three in a row (Tic-Tac-Toe style) |

### ✊ Rock-Paper-Scissors 20

| | |
|---|---|
| Players | 2 |
| Entry Cost | 20 Nix Coin |
| Type | Rock-Paper-Scissors |
| Rounds | 1 / 3 / 5 |

Moves are selected via the Game Panel; the player who wins more rounds wins the match.

### 💣 Minesweeper 20

| | |
|---|---|
| Players | 2 |
| Mines | 11 |
| Entry Cost | 20 Nix Coin |

Players search for mines; each mine found may create a chance to continue playing. The player who finds more mines wins.

### 🎲 Game 20

| | |
|---|---|
| Players | 2 |
| Entry Cost | 20 Nix Coin |

Once the second player joins, the system automatically determines the winner.

---

## Statistics & Leaderboards

### 🪙 Coin Leaderboard

| | |
|---|---|
| Persian | `آمار سکه` |
| English | `leaderboard` |
| Slash | `/leaderboard` |
| Purpose | Shows the Top 10 users by Nix Coin balance |
| Parameters | None |

### 🏆 Wins Leaderboard

| | |
|---|---|
| Persian | `آمار برد` |
| English | `leaderboard_wins` |
| Slash | `/leaderboard_wins` |
| Purpose | Shows the Top 10 users by recorded game wins |
| Parameters | None |

---

## Administration

Coming Later

---

## Common Errors

**Missing Required Parameters**
```text
transfer 123
```
Correct syntax:
```text
transfer 123 50
```

**Invalid Numeric Value**
```text
transfer 123 fifty
```

**Incorrect Parameter Order**
Order must follow `transfer <user> <amount>`.

**Incorrect Spacing**
```text
transfer12350
```

**Literal Placeholders**
`transfer <user> <amount>` is a syntax template — replace it with real values.

---

## Notes

- This file is public documentation only.
- No private information (tokens, API keys, database details, etc.) is included.
- `<...>` must always be replaced with an actual value.
- Parameter order matters for every command.
- Any capability not documented here is not an official feature.
- The Administration section is currently `Coming Later`.

---

## Command Reference

| Feature | Persian | English | Slash |
|---|---|---|---|
| 💰 Balance | موجودی | `balance` | `/balance` |
| 👤 Profile | پروفایل / حساب کاربری | `profile` | `/profile` |
| 💸 Transfer | انتقال | `transfer` | `/transfer` |
| 🎛️ Panel | پنل | `panel` | `/panel` |
| 🎁 Daily | روزانه | `daily` | `/daily` |
| 🏅 Level | سطح من | `level` | `/level` |
| 🪙 Coin Leaderboard | آمار سکه | `leaderboard` | `/leaderboard` |
| 🏆 Wins Leaderboard | آمار برد | `leaderboard_wins` | `/leaderboard_wins` |

[⬆ Back to top / بازگشت به بالا](#-self-nix--commands)


---

<p align="center">
  <a href="./README.md">
    <img src="https://img.shields.io/badge/⬅️_Back_to_Home-2ea44f?style=for-the-badge" alt="Back to README">
  </a>
</p>
