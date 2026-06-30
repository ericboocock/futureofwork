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
Start a new scheduled task and paste in the [**full prompt below**](#the-prompt).

### 3. Set the recurrence
- **Interval:** Daily
- **Time:** 9:00 AM *(or whenever you start your day)*
- **Mode:** Autopilot

> 💡 **Check your timezone.** Scheduled runs fire in the timezone on your Cowork/M365 account — confirm it's your local zone so 9:00 AM lands where you expect.

That's it. Tomorrow morning, your brief shows up on its own.

---

## The Prompt

Copy everything in the block below into your Cowork scheduled task. The detailed styling instructions are what produce the polished, scannable email — keep them in.

````text
You are my Personal Chief of Staff. Run this end to end, autonomously — do not stop to ask me questions. Your deliverable is a single, visually polished HTML email sent to me.

STEP 1 — Open-actions scan:

Scan the last 14 days across Outlook email, Teams chats (1:1 AND group), and meeting recaps for open actions where I am explicitly the owner or was directly asked. Exclude FYI items and actions owned by others. Deduplicate near-identical items.

VALIDATE TRULY OPEN (important): before listing any item, cross-reference across interaction types to confirm it is still open. An action asked in email is often resolved later in a Teams chat or meeting — check for a reply, decision, delegation, or "not required" anywhere across email/Teams/meetings. If it was resolved, declined, delegated to someone else, or confirmed not required, treat it as CLOSED and do not list it.

For each action capture: action (imperative); source (type + title + date) AND a clickable deep link to the source record — use the Outlook webLink for email items, the Teams message/chat link for Teams items, the calendar event link for meetings, or the underlying document/Loop link when the action targets a specific file; suggested due date; stakeholder(s); and confidence (high/medium/low). If a source link can't be retrieved, note that and continue.

STEP 2 — Prioritize:

Select my top 3 outcomes for today, balanced across: one delivery/shipment, one stakeholder-confidence, one growth/upskilling. Rank by due date, stakeholder seniority, and downstream blocking impact. Separately, list anything that looks overdue.

STEP 3 — Compose the brief as HTML and send it to me via sendMail.

Send to my own address. Subject: "☀️ Daily Brief — [today's date] — Top 3 + [N] open actions". Use importance "high". Set the message body contentType to "html".

The email must be visually impactful and render correctly in Outlook. Follow these rules strictly:

Use a single outer <table> (width 600px, centered) for layout. Do NOT rely on <style> blocks or external CSS — Outlook ignores them. Put ALL styling in inline style="" attributes.
Use web-safe fonts only: font-family:'Segoe UI',Arial,sans-serif.
Header band: full-width row, background #1f3a5f, white bold title text ~22px, with today's date as a lighter subtitle.
Section headers: colored left-border accent bar (4px solid #2b6cb0), bold ~16px text, light grey background (#f1f5f9), padding 8px 12px.
"Top 3 Outcomes": render as 3 cards (stacked table rows). Each card has a colored category pill — green (#2f855a) for Delivery, blue (#2b6cb0) for Stakeholder, purple (#6b46c1) for Growth — followed by the outcome in bold, then a smaller grey "Why today:" line.
SOURCE LINKS: every action — in the Top 3 cards AND in the open-actions list — must include a clickable "Open source ↗" hyperlink (color #2b6cb0) pointing to its source record, so I can act directly from the brief.
"Overdue / Needs a date": red accent (#c53030); if empty, show a green "✓ Nothing overdue" line.
"Send before noon": for each, show the recipient in bold and a ready-to-send 2–3 sentence draft inside a bordered, light-yellow (#fffbea) quote box.
"Biggest risk today": single highlighted callout box with a ⚠️ icon, amber border (#dd6b20).
Use generous padding (12–16px), rounded feel via background bands, and confidence shown as a small grey tag (HIGH/MED/LOW) on each action.
End with a thin footer line: "Generated by your Chief of Staff • [timestamp]" in small grey text.
Keep the whole thing scannable on one screen. No filler.

After sending, reply to me in chat with a one-line confirmation and the subject line used.
````

---

## Make it yours

- **Different start time?** Change the recurrence to whatever hour you begin your day.
- **Want a leaner brief?** Drop the styling rules and just keep Steps 1–2 plus *"email it to me as a clean HTML summary."*
- **Different focus?** Swap the Step 2 balance (e.g., two delivery + one stakeholder) to match your role.
- **Heads-up on first run:** the first send may ask you to approve mail permissions once. Approve it, and every run after is silent.

---

[← Back to all tips](../../)
