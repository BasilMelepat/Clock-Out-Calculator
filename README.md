# ⏰ Clock me Out

![Version](https://img.shields.io/badge/version-v2.266-4FA8E8)
[![Live demo](https://img.shields.io/badge/live%20demo-vercel-000000?logo=vercel)](https://clock-out-calculator.vercel.app)
[![License: CC0-1.0](https://img.shields.io/badge/license-CC0%201.0-lightgrey)](https://github.com/BasilMelepat/Clock-Out-Calculator/blob/main/LICENSE)
![Single file](https://img.shields.io/badge/single--file-HTML%20%2F%20JS-0B2A4A)
![No build](https://img.shields.io/badge/build-none-1E8E5A)

A work-hours companion that tells you **when you can clock out**. Enter your shift start, your breaks and your target hours, and it works out your clock-out time, counts down to it live, and keeps track of the hours you're ahead or behind across the month.

The whole app is **one HTML file**. No build step, no framework, no server, no account.

**🔗 Live app: [clock-me-out.vercel.app](https://clock-me-out.vercel.app)**

👨‍💻 Developed by **Basil Melepat**.

**Current version: v2.266** (shown in the badge at the top of the app; tap it to reload the page)

---

## Features

### Core
- **Clock-out calculator** from your clock-in time, breaks and target hours (target capped at 24 h).
- **Running Late Balance** to add make-up minutes to today's target.
- **Departure Planner** to plan an early departure and see the impact on your hours.

### 💼 Shift Details
- Current shift details with a collapsible card. "Add Shift Details" starts with the current time.
- A **log-balance chip** (ahead / behind) that pops in with an animation. Tap it to add backlog to today or to plan an early departure.
- **Live Clock card:** an analog dial, a big rolling `HH:MM:SS left` counter, and a status pill (Working, On break, Goal reached). A second amber pill shows when backlog has been added to today's target.
- **Clock-Out Time card:** celebration bubbles that multiply the longer you stay past your target, plus extra counters.
- **Welcome guide:** the greeting and sub-line follow the time of day, the day of the week and how close you are to your target. The sub-line tells you what to do next (backlog added, add backlog, you can leave early, backlog covered).

### 📅 Daily Log
- Add a day with its hours (a date is required).
- **Calendar View** and **Table View** side by side. Calendar days are tinted green when ahead and amber when behind, and today fills as your shift progresses.
- **Bulk import** from several Excel files and sheets at once, and a **Clear month** button.
- Only the **current calendar month** counts toward the balance and backlog.

### 📊 Overview
- Your name, picked up from the Excel upload (or set in Settings).
- Month tiles and a month dropdown.
- **Month Goal** with holidays and absences.
- **Weekday Pattern** and **Past Months** (last 12).
- **Settings** (collapsed by default): name, pointer effects, sound, backup and restore, and **🚽 Flush Everything**.

### Extras
- 🔔 **Sound effects** (synthesized, no audio files) for reaching your target, covering your backlog and hitting a planned departure time. Switch on or off in Settings.
- 🌗 Light and dark themes.
- 🖱️ Optional desktop pointer effects: custom cursor, cursor trail, spotlight glow, magnetic buttons and 3D card tilt.
- 📱 Fully responsive. On touch devices you can **swipe left or right to switch tabs**, and backup and restore are hidden.
- 🌙 **Midnight reset:** the shift clears when a new day starts, unless an overnight shift is still running. It then clears at the first midnight after it ends.

---

## Getting started

**Use it online:** open [clock-out-calculator.vercel.app](https://clock-out-calculator.vercel.app). On a phone, you can add it to your home screen from the browser menu.

**Or run it locally:**
1. Download `clock-out-calculator-v2.html`.
2. Open it in any modern browser.

Then tap **➕ Add Shift Details**, check your clock-in time and add any breaks. Your clock-out time appears right away.

**Deploying your own copy:** the app is a single static file, so any static host works. The live version runs on [Vercel](https://vercel.com): import the repository, and make sure the file is served as `index.html` (rename it, or add a rewrite). GitHub Pages and Netlify work the same way.

> **Internet:** only Excel import needs a connection. The spreadsheet library (SheetJS) is loaded from cdnjs the first time you import.

---

## Data and privacy

Everything stays **in your browser** (`localStorage`). Nothing is uploaded, and there is no analytics or tracking.

| Key | What it stores |
|---|---|
| `cmoShiftState` | Current shift: clock-in, target hours, breaks |
| `cmoLogEntries`, `cmoLogEntryCount` | Daily Log |
| `cmoHolidays`, `cmoAbsent` | Holidays and absent days |
| `cmoUserName` | Your name |
| `cmoTheme`, `cmoView`, `cmoFx`, `cmoSound` | Preferences (kept when you flush data) |

**Backup and restore** (desktop only) saves logs, shift, holidays, absences and name to a JSON file. Restoring replaces everything currently saved.

Clearing your browser's site data removes your logs, so download a backup now and then.

---

## Versioning

- Each update request bumps the **patch number** (v2.265 to v2.266).
- The version badge sits in the header. **Click it to reload** the page.
- Updates are delivered as the full HTML file.

### Recent changes

| Version | Change |
|---|---|
| v2.266 | Sound effects with a Settings switch |
| v2.265 | New calendar hover: tile morphs to a circle with a ring pulse |
| v2.263–v2.264 | Softer, cleaner calendar design and hover |
| v2.260 | Welcome sub-line becomes a guide (backlog and early departure) |
| v2.259 | "Backlog added" pill on the Live Clock |
| v2.257–v2.258 | Welcome message follows the target, with backlog encouragement |
| v2.255 | Midnight reset with overnight-shift protection |
| v2.249 | Swipe to switch tabs on mobile |
| v2.248 | Settings collapses in place; backup and restore hidden on mobile |
| v2.246–v2.247 | Mobile full-width header |

---

## Project layout

```
clock-out-calculator-v2.html   # the entire app (HTML, CSS and JS)
LICENSE                        # CC0 1.0 Universal
README.md
```

## About the developer

Clock me Out is designed and built by **Basil Melepat**, a designer turned developer. It started as a small tool to answer one question, "when can I go home?", and keeps growing with every new idea.

## Contributing

This is a hobby project with no finish line: new ideas keep landing. Issues and suggestions are welcome. Please keep it a single file and keep it working on phones.

## License

This project is released into the public domain under the [**CC0 1.0 Universal**](https://github.com/BasilMelepat/Clock-Out-Calculator/blob/main/LICENSE) dedication. You can copy, modify, host and use it for any purpose, including commercial use, without asking permission. Credit is appreciated but not required.

Created by Basil Melepat, 2026.
