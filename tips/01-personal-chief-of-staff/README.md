# Tip #01 — Personal Chief of Staff 🎯

> Every morning, before I open a single app, a brief is already in my inbox.

It reads my work signals, finds everything that actually needs *my* attention, and hands me a prioritized plan:

- 🎯 **My top 3 outcomes** for the day — balanced across one delivery, one stakeholder, one growth item
- 📌 **What's slipping** and needs a new date
- ✍️ **The stakeholder notes** I should send before noon — already drafted, ready to send
- ⚠️ **The one risk** most likely to derail my day, and how to get ahead of it
- 🔗 **A click-through link** on every action — straight to the source email, Teams message, or meeting, so I can act without hunting for it

No code. No infrastructure. It runs entirely inside **Microsoft Copilot Cowork**, scans **WorkIQ** for anything requiring my attention across email, Teams, and meetings, then emails me a clean, visually formatted brief I can act on in 60 seconds.

It's the difference between *reacting* to my day and *running* it.

---

## What you need

- **Microsoft 365 Copilot** with access to **Cowork**
- **WorkIQ** connected (so it can read your email, Teams, and meeting recaps)
- 2 minutes to set it up

---

## Setup

### 1. Open Cowork
In Microsoft 365 Copilot, open the **Cowork** app (left rail / app launcher).

### 2. Create a scheduled task
Start a new scheduled task and paste in the [**full prompt** (`prompt.md`)](./prompt.md).

### 3. Set the recurrence
- **Interval:** Daily
- **Time:** 9:00 AM *(or whenever you start your day)*
- **Mode:** Autopilot

> 💡 **Check your timezone.** Scheduled runs fire in the timezone on your Cowork/M365 account — confirm it's your local zone so 9:00 AM lands where you expect.

That's it. Tomorrow morning, your brief shows up on its own.

---

## The Prompt

The full, copy-paste prompt lives in one place so it never drifts:

### 📋 **[`prompt.md` — copy it here](./prompt.md)**

The detailed styling instructions in that file are what produce the polished, scannable email — keep them in when you paste.

---

## Make it yours

- **Different start time?** Change the recurrence to whatever hour you begin your day.
- **Want a leaner brief?** Drop the styling rules and just keep Steps 1–2 plus *"email it to me as a clean HTML summary."*
- **Different focus?** Swap the Step 2 balance (e.g., two delivery + one stakeholder) to match your role.
- **Heads-up on first run:** the first send may ask you to approve mail permissions once. Approve it, and every run after is silent.

---

[← Back to all tips](../../)
