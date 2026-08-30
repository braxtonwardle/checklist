[README.md](https://github.com/user-attachments/files/31498929/README.md)
# Weekly Board

A personal daily/weekly habit tracker — single self-contained HTML file, no build step, no backend, no login. All data lives in the browser's `localStorage`, so nothing leaves the device it's used on.

Live at: `https://<your-username>.github.io/<repo-name>/`

## Features

- **Weekday checklist** — a fixed set of daily items (wake time, water, dog walk, sleep, chess study, a rotating chore, phone/bedtime), plus a dedicated workout slot
- **Scheduled workout days** — Monday/Wednesday/Thursday, each tied to a specific lift/cycle day. A missed day gets one shot at a makeup the next eligible day; Friday can absorb a missed Wednesday or Thursday (or become a free-choice "catch-up" day if both were missed). Tuesday is always a rest day — no exceptions, no makeup slot.
- **Rotating chore pool** — cycles through a small set of chores rather than one static "clean" item; a trash-specific chore is restricted to its actual pickup window so it never shows up on a day it can't be done.
- **Weekend mode** — Saturday and Sunday each render as their own day, with their own progress count and sick/vacation skip, while a set of extra items (physical activity, weekly clean, chess study, reading) stays shared across the whole weekend. A "Sophie weekend" mode hides the extra items entirely for a lighter weekend.
- **Weekly counters** — meditation and home-cooked-meals targets (×3/week), tracked as dot progress rather than daily checkboxes.
- **Streaks** — shown per daily item (weekday and weekend alike) and per weekly counter. A day marked "sick / traveling" pauses a streak instead of breaking it; an in-progress day/week is never treated as a miss before it's actually over.
- **Sunday recap** — a summary panel that appears only when viewing Sunday: one completion percentage across the whole week (all 7 days, skipped days excluded), plus the week's meditation and cooking counts.
- **Daily quote** — rotates by calendar date from a fixed bank of real, attributed quotes (no AI-generated or "in the style of" content — every attributed line is genuine).
- **7-day history strip** — at-a-glance view of recent completion, with distinct styling for skipped/sick days.
- **CSV export** — pulls the weekday checklist history out of `localStorage` for review elsewhere.
- **JSON backup/restore** — downloads the complete app state as one file and can reload it back in, so a cleared browser or a new device doesn't lose history. A status line next to the button shows how long it's been since the last backup.

## Tech

Vanilla HTML/CSS/JS. No frameworks, no npm packages, no build tooling. Everything — including the custom home-screen icon — is embedded directly in the single `index.html` file.

## Using it day to day

Open the page (or the installed home-screen icon), check things off. Data is saved automatically after every change — nothing to submit or sync. Data is local to whichever browser/device it's opened in; it does not sync across devices.

## Editing

This is a hand-maintained single file. Changes are made directly to `index.html` and redeployed — there's no separate source/build step.
