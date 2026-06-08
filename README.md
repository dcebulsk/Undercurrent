# ◆ UNDERCURRENT

**A synthwave-themed personal productivity RPG.**

Track your goals, habits, tasks, and energy. Earn XP. Level up. Build momentum.

🌐 **Live app:** [dcebulsk.github.io/Undercurrent](https://dcebulsk.github.io/Undercurrent)

---

## What It Is

UNDERCURRENT turns daily productivity into a game. Your habits build streaks. Your tasks earn XP. Your focus sessions push your goals forward. Everything feeds into a single levelling system that reflects how consistently you show up.

Built as a single HTML file with no framework — just vanilla JS, Firebase, and a lot of iteration.

---

## Features

### ◆ Currents (Goals)
Long-term goals with progress tracking, XP bars, and subgoals. Link habits and tasks to a Current so completions push it forward. A default **Energy Level Check-in** current tracks your daily check-in streak.

### ◎ Habits
Daily habits with scheduling (Mon–Sun), streaks, difficulty levels, and consistency multipliers. Habits not scheduled for the current day are greyed out. Supports rollover debt and weekly average streak types.

- **Drag to reorder** — grab the ⠿ handle to rearrange
- **Active days display** — M T W T F S S shown next to each streak
- **Yesterday popup** — on first open each day, prompts you to log any habits you may have completed yesterday
- **Label filtering** — filter by Work, Gamedev, Health, etc.

### ◻ Tasks
Priority-based task list (High / Medium / Low) with due dates and Current linking. Completed tasks auto-sort to the bottom.

- **Current Tasks (max 3)** — pin up to 3 tasks for today's focus, inspired by *Four Thousand Weeks*. Completing a task auto-removes it after 3 seconds with an undo option.
- **Drag to reorder**
- **Label filtering**

### ◷ Focus (Pomodoro)
Configurable focus sessions with consecutive session planning, break intervals, and session logging. Each completed session awards XP and pushes any linked Current forward.

### ⚡ Energy Check-ins
Log how you're feeling throughout the day using a 5-level traffic light model:

| Level | Description |
|---|---|
| 🔴 Depleted | Running on fumes. Basic tasks feel hard. Rest is the priority. |
| 🟠 Low | Sluggish but functional. Getting through the day, not thriving. |
| 🟡 Steady | Neutral baseline. Capable, nothing special. Showing up. |
| 🟢 Good | Clear-headed and motivated. Things are flowing. |
| ⚡ Peak | Everything clicks. High focus, high drive. Make the most of it. |

Tap any level directly on the Energy page to log a check-in. Factors (Exercise, Sleep, Stress, etc.) are colour-coded positive/negative/neutral. All-day factors (📌) auto-carry into every check-in that day. Goal: 3 check-ins per day for a +50 XP bonus.

### 📊 Review
Weekly summary showing this week vs last week habit completion, a day-by-day bar chart, on-pace projection, today's energy check-ins, and XP progress for all Currents.

---

## XP & Levelling

| Action | XP |
|---|---|
| Easy habit | +15 |
| Medium habit | +30 |
| Hard habit | +50 |
| Low priority task | +15 |
| Medium priority task | +25 |
| High priority task | +40 |
| 25-min focus session | +75 |
| 50-min focus session | +150 |
| 3 energy check-ins/day | +50 |

XP thresholds follow an Option E curve: 150 → 400 → 800 → 1,400 → 2,200 → 3,500 → 5,500 → 8,500 → 13,000 → 20,000…

---

## Settings

- **Colour schemes** — Synthwave (default), Midnight Green, Crimson, Ocean Blue, Amber, Light
- **Text size** — Small / Normal / Large / X-Large
- **Labels** — create shared filter tags for habits and tasks
- **Energy factors** — customise the factor list
- **Quotes** — add your own quotes, shown on the Currents page
- **Export / Import** — download your data as JSON or restore from backup

---

## Sync & Accounts

Sign in with Google to sync your data across all devices. Data is stored in Firebase Firestore — only you can access your own data.

- Auto-saves 1.5 seconds after any change
- Manual sync button (⟳) in the topbar with 5-second cooldown
- Loads fresh data on every page open
- Theme, text size, and section collapse states sync across devices

**Offline mode** — tap "Use without account" to run locally only (data stays in the browser).

---

## Sounds

| Event | Sound |
|---|---|
| Habit / task completed | Random from 3 upbeat sounds |
| Pomodoro session complete | Random from 2 glassy bell sounds |
| Level up | Achievement chime |

---

## Tech Stack

| Layer | Tech |
|---|---|
| App | Vanilla HTML / CSS / JavaScript (single file) |
| Auth | Firebase Authentication (Google Sign-In) |
| Database | Firebase Firestore |
| Hosting | GitHub Pages |
| PWA | Web App Manifest + Service Worker |

No build step. No framework. No dependencies beyond Firebase.

---

## Files

Upload all of these to the repo root for a full deployment:

```
index.html          — the entire app
manifest.json       — PWA manifest
sw.js               — service worker
icon-192.png        — app icon
icon-512.png        — app icon (large)
favicon-32.png      — browser tab icon
snd_bells_a.wav     — pomodoro sound A
snd_bells_b.wav     — pomodoro sound B
snd_chirpy.wav      — completion sound
snd_happy.wav       — completion sound
snd_synthetic.wav   — completion sound
snd_levelup.wav     — level up sound
```

---

## Roadmap

- Rewards system (self-defined XP thresholds)
- Streak decay logic
- Weekly average habit target frequency + progress bar
- Milestone badges
- Factor correlation trends (needs 30+ days of data)
- Recurring tasks

---

## Inspiration

The **Current Tasks (max 3)** system is directly inspired by Oliver Burkeman's *Four Thousand Weeks: Time Management for Mortals* — the idea that choosing three things to focus on today, and accepting you can't do everything, is more honest and more effective than an infinite to-do list.

---

*Built iteratively with Claude.*
