# 🤖 Self Nix — Commands

> Complete public command documentation for Self Nix.

---

## 📚 Table of Contents

- [🚀 Getting Started](#-getting-started)
- [📖 Command Structure](#-command-structure)
- [🧩 Parameters & Arguments](#-parameters--arguments)
- [👤 Account](#-account)
  - [موجودی / Balance](#1-موجودی--balance)
  - [پروفایل / Profile](#2-پروفایل--profile)
  - [انتقال سکه / Transfer](#3-انتقال-سکه--transfer)
  - [پنل / Panel](#4-پنل--panel)
  - [روزانه / Daily](#5-روزانه--daily)
  - [سطح من / Level](#6-سطح-من--level)
- [🪙 Nix Coin](#-nix-coin)
- [🎮 Games](#-games)
  - [دوز 20](#-دوز-20)
  - [سنگچی 20](#-سنگچی-20)
  - [مین روب 20](#-مین-روب-20)
  - [بازی 20](#-بازی-20)
- [🏆 Statistics & Leaderboards](#-statistics--leaderboards)
  - [آمار سکه](#-آمار-سکه--coin-leaderboard)
  - [آمار برد](#-آمار-برد--wins-leaderboard)
- [🔐 Administration](#-administration)
- [⚠️ Common Errors](#️-common-errors)
- [💡 Notes](#-notes)
- [📋 Command Reference](#-command-reference)

---

# 🚀 Getting Started

Self Nix provides a collection of Telegram commands for managing account information, Nix Coin, Level progress, Daily rewards, games, and leaderboards.

Commands can be entered using their documented Persian or English form.

Where supported, commands can also be used with Telegram's `/` Slash Command format.

### Basic Examples

```text
موجودی

balance

/balance

All three forms above refer to the Balance command.

Commands that require parameters must be written according to their documented syntax.

For example:

transfer <user> <amount>

must be converted into a real command by replacing the placeholders:

transfer 123 50


---

📖 Command Structure

Commands can be divided into two main groups:

1. Commands without parameters


2. Commands with parameters




---

1. Commands Without Parameters

A command without parameters only requires the command itself.

Syntax

<command>

Example

balance

Slash form:

/balance

There is no additional value after the command.


---

2. Commands With One Parameter

A command may require one additional value.

Syntax

<command> <parameter>

<parameter> is a placeholder and must be replaced with the required value.

Example

<command> 123

Here:

<parameter>

has been replaced by:

123


---

3. Commands With Multiple Parameters

A command can require multiple values.

Syntax

<command> <parameter_1> <parameter_2>

Example:

transfer <user> <amount>

Real usage:

transfer 123 50

Slash usage:

/transfer 123 50

In this example:

123

is the user parameter and:

50

is the amount parameter.


---

🧩 Parameters & Arguments

Placeholder Syntax

Values written between < and > are placeholders.

They are not meant to be typed literally.

For example:

transfer <user> <amount>

means that the user must replace both placeholders with actual values.

Example:

transfer 123 50

Mapping:

<user>   → 123
<amount> → 50


---

Command Syntax Reference

Symbol	Meaning	Example

<user>	User target	123456789
<amount>	Numeric amount	50
<parameter>	Required input value	value
/	Telegram Slash Command prefix	/balance
@username	Telegram username target where supported	@username



---

📌 Parameter Rules

1. Spaces Between Command and Parameters

A space must separate the command from its parameters.

Correct:

transfer 123 50

Incorrect:

transfer12350

The command parser must be able to distinguish the command from each argument.


---

2. Parameter Order

Parameters must be provided in the order specified by the command syntax.

For:

transfer <user> <amount>

the first value represents the user and the second value represents the amount.

Correct:

transfer 123 50

The following interpretation is used:

123 → user
50  → amount


---

3. Numeric Parameters

When a parameter is documented as a numeric value, it must be provided as a number.

Correct:

transfer 123 50

Incorrect:

transfer 123 fifty


---

4. Username Parameters

Where username targeting is supported, a Telegram username can be represented using @.

Example:

@username

The exact target formats supported by a command are defined in that command's documentation.


---

5. Reply-Based Targeting

Some commands may support selecting a user by replying to their Telegram message.

Reply-based usage should only be considered supported where it is explicitly documented for the command.


---

6. Required Parameters

If a parameter is required, it must be provided.

For example:

transfer <user> <amount>

requires both:

<user>

and:

<amount>

Therefore:

transfer 123

is incomplete because the amount is missing.


---

7. Placeholder Values Must Be Replaced

Incorrect:

transfer <user> <amount>

Correct:

transfer 123 50

The placeholder notation is used only to describe the command structure.


---

👤 Account

Account commands provide access to account-related information and features.


---

1. 💰 موجودی / Balance

🇮🇷 فارسی

موجودی

🇬🇧 English

balance

/ Slash

/balance

🎯 کاربرد

دستور موجودی برای نمایش موجودی فعلی Nix Coin کاربر استفاده می‌شود.

این دستور اطلاعات مربوط به موجودی فعلی کاربر و ارزش آن را نمایش می‌دهد.

🧩 Syntax

موجودی

balance

/balance

🔢 Parameters

این دستور پارامتر اضافی ندارد.

🧪 Examples

موجودی

balance

/balance


---

2. 👤 پروفایل / Profile

🇮🇷 فارسی

پروفایل
حساب کاربری

🇬🇧 English

profile

/ Slash

/profile

🎯 کاربرد

دستور profile برای نمایش اطلاعات حساب Telegram و اطلاعات مرتبط با حساب Self Nix استفاده می‌شود.

اطلاعات پروفایل و تصویر کاربر نیز در این بخش نمایش داده می‌شود.

🧩 Syntax

پروفایل

حساب کاربری

profile

/profile

🔢 Parameters

این دستور پارامتر اضافی ندارد.

🧪 Examples

پروفایل

حساب کاربری

profile

/profile


---

3. 💸 انتقال سکه / Transfer

🇮🇷 فارسی

انتقال

🇬🇧 English

transfer

/ Slash

/transfer

🎯 کاربرد

دستور transfer برای انتقال Nix Coin از موجودی کاربر به یک کاربر دیگر استفاده می‌شود.

برای انتقال باید کاربر دریافت‌کننده و مقدار Nix Coin مشخص شود.

🧩 Syntax

انتقال <user> <amount>

transfer <user> <amount>

/transfer <user> <amount>

🔢 Parameters

Parameter	Type	Description

<user>	User	کاربر دریافت‌کننده
<amount>	Number	مقدار Nix Coin برای انتقال


👤 User

پارامتر <user> مشخص می‌کند Nix Coin برای چه کاربری ارسال شود.

کاربر دریافت‌کننده می‌تواند بر اساس شناسه یا username مشخص شود و در موارد پشتیبانی‌شده می‌تواند از طریق Reply نیز انتخاب شود.

🪙 Amount

پارامتر <amount> تعداد Nix Coin موردنظر برای انتقال را مشخص می‌کند.

این مقدار باید به‌صورت عدد وارد شود.

💳 Transfer Fee

انتقال Nix Coin دارای:

10%

کارمزد انتقال است.

بنابراین مبلغ ارسال‌شده، کارمزد و مبلغ نهایی دریافتی می‌توانند متفاوت باشند.

🧪 Examples

انتقال 123 50

transfer 123 50

/transfer 123 50

📤 Example Output

💸 انتقال سکه انجام شد

👤 دریافت کننده: کاربر
📤 مبلغ ارسال: 11
💳 کارمزد: 1
📥 مبلغ دریافتی: 10
♾️ موجودی شما: نامحدود
📅 تاریخ: 2026-09-25 16:47:15


---

4. 🎛️ پنل / Panel

🇮🇷 فارسی

پنل

🇬🇧 English

panel

/ Slash

/panel

🎯 کاربرد

دستور panel برای باز کردن پنل اصلی Self Nix استفاده می‌شود.

این پنل دسترسی سریع به قابلیت‌های حساب را فراهم می‌کند.

🧩 Syntax

پنل

panel

/panel

🔢 Parameters

این دستور پارامتر اضافی ندارد.

🧪 Examples

پنل

panel

/panel


---

5. 🎁 روزانه / Daily

🇮🇷 فارسی

روزانه

🇬🇧 English

daily

/ Slash

/daily

🎯 کاربرد

دستور daily برای استفاده از قابلیت Daily و دریافت پاداش روزانه استفاده می‌شود.

دریافت پاداش به واجد شرایط بودن کاربر بستگی دارد.

🧩 Syntax

روزانه

daily

/daily

🔢 Parameters

این دستور پارامتر اضافی ندارد.

🧪 Examples

روزانه

daily

/daily


---

6. 🏅 سطح من / Level

🇮🇷 فارسی

سطح من

🇬🇧 English

level

/ Slash

/level

🎯 کاربرد

دستور level برای مشاهده وضعیت Level و پیشرفت کاربر استفاده می‌شود.

اطلاعات اصلی این بخش شامل موارد زیر است:

Level فعلی

XP فعلی

مقدار XP موردنیاز برای Level بعدی

جایزه بعدی

اطلاعات مرتبط با پیشرفت کاربر


🧩 Syntax

سطح من

level

/level

🔢 Parameters

این دستور پارامتر اضافی ندارد.

🧪 Example

سطح من

یا:

level

📤 Example Information

🏅 Level: 1
⭐ XP: 0

⬆️ تا Level 2: 500 XP
🎁 جایزه بعدی: 🪙 10 سکه

📊 Account Statistics

ممکن است اطلاعات آماری مرتبط با حساب نیز در این بخش نمایش داده شود.

این اطلاعات می‌تواند شامل موارد زیر باشد:

گردش مالی

سکه خریداری‌شده

مبلغ خرید سکه

شارژ کیف پول

تعداد کانفیگ

حجم کانفیگ

تمدید

دعوت موفق

بازی ثبت‌شده

موجودی سکه

کیف پول



---

🪙 Nix Coin

Nix Coin ارز داخلی Self Nix است.

Nix Coin در بخش‌های مختلف سیستم، از جمله برخی قابلیت‌های بازی، مورد استفاده قرار می‌گیرد.

⏱️ Nix Coin Usage Rate

نرخ استفاده:

2 Nix Coins = 1 Hour

معادل‌های تعریف‌شده:

Duration	Nix Coins

1 Hour	2
12 Hours	24
24 Hours	48
7 Days	336
30 Days	1440


Quick Reference

2 Coins   = 1 Hour
24 Coins  = 12 Hours
48 Coins  = 24 Hours
336 Coins = 7 Days
1440 Coins = 30 Days


---

🎮 Games

Self Nix دارای بازی‌های دو نفره است.

هر بازی قوانین و هزینه ورود مخصوص خود را دارد.


---

🎯 دوز 20

بازی دو نفره شبیه Tic-Tac-Toe.

👥 Players

2 Players

🪙 Entry Cost

20 Nix Coin

🎯 هدف بازی

هدف بازی ساختن یک خط سه‌تایی است.

📋 مشخصات

Feature	Value

Players	2
Entry Cost	20 Nix Coin
Goal	ساخت یک خط سه‌تایی



---

✊ سنگچی 20

بازی دو نفره Rock-Paper-Scissors.

👥 Players

2 Players

🪙 Entry Cost

20 Nix Coin

🎮 انتخاب حرکت

حرکت بازیکنان از طریق پنل بازی انتخاب می‌شود.

🔄 تعداد راند

بازیکنان می‌توانند یکی از حالت‌های زیر را انتخاب کنند:

1 Round
3 Rounds
5 Rounds

🏆 تعیین برنده

بازیکنی که راندهای بیشتری را برنده شود، برنده بازی خواهد بود.

📋 مشخصات

Feature	Value

Players	2
Entry Cost	20 Nix Coin
Game Type	Rock-Paper-Scissors
Rounds	1 / 3 / 5
Move Selection	Game Panel



---

💣 مین روب 20

بازی دو نفره به سبک Minesweeper.

👥 Players

2 Players

💣 Mines

11 Mines

🪙 Entry Cost

20 Nix Coin

🎯 نحوه بازی

بازیکنان در جریان بازی مین‌ها را پیدا می‌کنند.

هر مین پیداشده می‌تواند فرصت ادامه بازی ایجاد کند.

🏆 تعیین برنده

بازیکنی که تعداد بیشتری مین پیدا کند، برنده بازی است.

📋 مشخصات

Feature	Value

Players	2
Mines	11
Entry Cost	20 Nix Coin
Game Type	Minesweeper-style



---

🎲 بازی 20

یک بازی دو نفره سریع.

👥 Players

2 Players

🪙 Entry Cost

20 Nix Coin

🎯 نحوه تعیین برنده

پس از ورود بازیکن دوم، سیستم به‌صورت خودکار برنده را مشخص می‌کند.

📋 مشخصات

Feature	Value

Players	2
Entry Cost	20 Nix Coin
Result	Automatically determined after the second player joins



---

🏆 Statistics & Leaderboards

بخش Statistics شامل رتبه‌بندی کاربران بر اساس اطلاعات ثبت‌شده در Self Nix است.


---

🪙 آمار سکه / Coin Leaderboard

🇮🇷 فارسی

آمار سکه

🇬🇧 English

leaderboard

/ Slash

/leaderboard

🎯 کاربرد

نمایش Top 10 کاربران بر اساس مقدار Nix Coin.

🧩 Syntax

آمار سکه

leaderboard

/leaderboard

📊 Result

نتیجه شامل رتبه‌بندی Top 10 کاربران بر اساس مقدار Nix Coin است.

🔢 Parameters

این دستور پارامتر اضافی ندارد.


---

🏆 آمار برد / Wins Leaderboard

🇮🇷 فارسی

آمار برد

🇬🇧 English

leaderboard_wins

/ Slash

/leaderboard_wins

🎯 کاربرد

نمایش Top 10 کاربران بر اساس تعداد بردهای ثبت‌شده در بازی‌ها.

🧩 Syntax

آمار برد

leaderboard_wins

/leaderboard_wins

📊 Result

نتیجه شامل رتبه‌بندی Top 10 کاربران بر اساس تعداد بردهای ثبت‌شده در بازی‌ها است.

🔢 Parameters

این دستور پارامتر اضافی ندارد.


---

🔐 Administration

Coming Later

Administration documentation will be added later.

No administration command is documented in this version.


---

⚠️ Common Errors

Missing Required Parameters

اگر دستوری به پارامتر نیاز داشته باشد و پارامتر موردنیاز ارسال نشود، دستور ناقص خواهد بود.

Syntax

transfer <user> <amount>

Incomplete

transfer 123

در این مثال مقدار <amount> وارد نشده است.

Correct

transfer 123 50


---

Invalid Numeric Value

پارامترهایی که به‌عنوان مقدار عددی تعریف شده‌اند باید به‌صورت عدد وارد شوند.

Correct

transfer 123 50

Incorrect

transfer 123 fifty


---

Incorrect Parameter Order

ترتیب پارامترها باید مطابق Syntax مستندشده باشد.

Syntax

transfer <user> <amount>

Correct

transfer 123 50

در این مثال:

123 → User
50 → Amount


---

Incorrect Spacing

پارامترها باید با فاصله از command جدا شوند.

Correct

transfer 123 50

Incorrect

transfer12350


---

Literal Placeholders

مقادیر داخل < > فقط برای نمایش ساختار command هستند.

Incorrect

transfer <user> <amount>

Correct

transfer 123 50


---

Unsupported Syntax

هر command فقط syntaxهایی را پشتیبانی‌شده در نظر می‌گیرد که در مستندات همان command ذکر شده باشند.

نباید syntax جدیدی بر اساس حدس ساخته شود.


---

💡 Notes

COMMANDS.md فقط مستندات عمومی Self Nix را ارائه می‌کند.

هیچ Token، API Key، اطلاعات دیتابیس یا Source Code خصوصی در این مستندات قرار نمی‌گیرد.

دستورات فارسی و انگلیسی در کنار Slash Command مربوط به خود نمایش داده شده‌اند.

/ نشان‌دهنده Telegram Slash Command است.

مقادیر داخل < > باید با مقدار واقعی جایگزین شوند.

ترتیب پارامترها مهم است.

فاصله بین command و پارامترها مهم است.

مقادیر عددی باید به‌صورت عدد وارد شوند.

@username فقط در مواردی قابل استفاده است که username به‌عنوان target پشتیبانی شود.

Reply فقط در commandهایی قابل استفاده است که از Reply پشتیبانی می‌کنند.

قابلیت‌هایی که در این فایل مستند نشده‌اند، نباید به‌عنوان قابلیت رسمی Self Nix در نظر گرفته شوند.

بخش Administration فعلاً مستند نشده و فقط به‌صورت Coming Later مشخص شده است.

مقادیر و اطلاعات نمایش داده‌شده در مثال‌ها صرفاً نمونه‌ای برای توضیح ساختار خروجی هستند.



---

📋 Command Reference

Feature	فارسی	English	Slash

💰 موجودی	موجودی	balance	/balance
👤 پروفایل	پروفایل / حساب کاربری	profile	/profile
💸 انتقال	انتقال	transfer	/transfer
🎛️ پنل	پنل	panel	/panel
🎁 روزانه	روزانه	daily	/daily
🏅 سطح	سطح من	level	/level
🪙 آمار سکه	آمار سکه	leaderboard	/leaderboard
🏆 آمار برد	آمار برد	leaderboard_wins	/leaderboard_wins



---

📌 Quick Syntax Reference

No Parameters

<command>

Example:

balance

Slash:

/balance


---

One Parameter

<command> <parameter>

The placeholder must be replaced with the actual value.


---

Multiple Parameters

<command> <parameter_1> <parameter_2>

Example:

transfer <user> <amount>

Real command:

transfer 123 50

Slash command:

/transfer 123 50


---

📖 Complete Command List

موجودی
balance
/balance

پروفایل
حساب کاربری
profile
/profile

انتقال <user> <amount>
transfer <user> <amount>
/transfer <user> <amount>

پنل
panel
/panel

روزانه
daily
/daily

سطح من
level
/level

آمار سکه
leaderboard
/leaderboard

آمار برد
leaderboard_wins
/leaderboard_wins


---

🤖 Self Nix

Public Command Documentation
