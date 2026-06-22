# Lift — Workout Project

A self-contained personal workout app + plan. Everything here is local: open it offline, no internet needed.

Built around: ~235 lb / 5'11" / getting back in shape. Goal = lose fat and tighten the chest, broaden arms and shoulders. Gear = 25 lb + 11 lb dumbbell pairs, a bench, a bike + indoor cycle. ~1 hr/day.

## What's in here

```
Lift-Workout/
├── index.html             ← the app (uses the local images folder). This is what GitHub Pages serves.
├── Lift-Standalone.html   ← the SAME app, with every image baked inside the file.
│                            One portable file. AirDrop THIS to your iPhone for full offline use.
├── Exercise-Plan.md       ← the written plan (schedule, cheat sheet, demos). Markdown.
├── images/
│   ├── icon.png           ← home-screen app icon
│   └── exercises/         ← 44 demo photos (start + finish for all 22 moves)
├── data/
│   └── program.json       ← the raw data: every exercise, its photos, and the weekly schedule
└── README.md              ← this file
```

## Using it on your iPhone

AirDrop **`Lift-Standalone.html`** (not Lift.html, it needs the images folder next to it). On the phone:
1. Open it from Files, it opens in Safari.
2. Share icon → **Add to Home Screen**.
3. Launch from the icon, it runs fullscreen like an app, fully offline.

## Live site

Hosted with GitHub Pages at: **https://justintylerm.github.io/lift/**
Open that on your iPhone, then Share → Add to Home Screen.

## Using it on your computer

Just double-click **`index.html`**. It pulls photos from the `images/` folder, so keep them together.

## How it works

- Tap a day tab up top (it opens to today). Tap the set bubbles as you finish each set; progress saves automatically.
- **Show me how** on any exercise shows the start/finish photos + a form cue.
- **Edit** (top right) lets you reorder, add, remove, or change sets/reps right on the phone.
- **ⓘ** button = cheat sheet + a "reset to original plan" button.

## Editing the plan (the "brain")

Open `index.html` (or the standalone) in a text editor. The top of the `<script>` has a clearly commented config:
- **`LIBRARY`** — the dictionary of exercises (name → 2 photos + a form cue).
- **`WEEK`** — the schedule. Each exercise is one line: `["Name", sets, "reps", "note"]`. Cut/paste lines to move them, add a line to add a move.

`data/program.json` is the same data in plain JSON if you'd rather read/version it there.

## Photo credit

Exercise photos are from the **free-exercise-db** (https://github.com/yuhonas/free-exercise-db), released into the public domain (Unlicense). Downloaded and stored locally here so the project works offline.
