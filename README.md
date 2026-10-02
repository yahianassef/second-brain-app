# Second Brain

One page that holds the things a productivity app usually spreads across five:
projects, tasks, habits, studying, exercising, finances, a journal, courses,
notes, and a map of how all of it connects.

It runs in your browser. There is no server, no account, and nothing is sent
anywhere unless you switch on a sync you control. Open the file, start typing.

**[Try it](https://yahianassef.github.io/second-brain-app/)** — nothing to install, nothing to sign up for.

---

## What is in it

| | |
|---|---|
| **Dashboard** | Today at a glance: what is due, what you have logged, where the month stands. |
| **Map** | Everything you keep, drawn as a graph. Drill from a kind of thing, to one thing, to what it touches. `[[Double brackets]]` link by title, the way Obsidian does, and you can draw your own links. |
| **Projects & tasks** | Priorities, deadlines, progress, a board, and tasks that belong to projects. |
| **Habits** | A daily grid, streaks, and a heatmap of the month. |
| **Studying & exercising** | Sessions and workouts against a weekly target — plus a library of **208 exercises** with instructions, form tips, common mistakes and a video for each, and six programmes that drill from plan to day to movement. |
| **Finances** | Income, spending, budgets, savings goals, and credit cards whose charges only count as spending once you mark them paid. |
| **Journal** | An entry a day with mood, a streak, and a calendar. |
| **Notes** | Categories, pinning, and to-do lists: write `- [ ] something` and it becomes a box you can tick. |
| **Car maintenance** | Fuel and service logs with cost per kilometre — optional, and driven by a Google Sheet. |

Everything is searchable from one box (`Ctrl K`), and exports to CSV or JSON
whenever you want to leave.

## Themes

Light, dark, or whatever your device is set to, in six accent colours. The
whole app recolours: buttons, charts, progress rings, heatmaps. There is a
living background of drifting, linked points, numbers that count up rather than
snap, and a small burst when you finish something — each of which you can
switch off, and all of which stop for `prefers-reduced-motion`.

## Two builds, one brain

- `app.html` — the laptop build, with a sidebar and keyboard shortcuts.
- `m.html` — the phone build, with bottom tabs, sheets and a home-screen icon.

They share their data and every module between them, so a change lands in both.
`index.html` sends you to whichever suits the device you are on.

## Your data

It lives in your browser's local storage, which means it is on your device and
nowhere else. Three optional ways to move it:

1. **Export** — JSON for a full backup, CSV per section for a spreadsheet.
2. **A private GitHub gist** — paste a token with only the `gist` scope and your
   devices merge item by item, newest edit winning, deletions remembered.
3. **Google Sheets** — a small Apps Script of your own (in `apps-script/`) so
   expenses, fuel and services live in spreadsheets you already keep.

Nothing is enabled by default. No analytics, no telemetry, no third-party
scripts — [check for yourself](app.html), it is one file.

### Accounts, if you want them

`supabase/` has everything needed to run this for more than one person: a
schema with row-level security so an account can only ever read its own rows,
and a client that signs people up, signs them in and syncs per item. Point
`cloud-config.js` at a Supabase project and the app grows a sign-in screen and
an account menu. Leave it as it is and the app stays local-first.

## Running it

Open `app.html`. That is the whole installation.

To put it online, this repository is already a static site — fork it, turn on
GitHub Pages, and your copy lives at `https://<you>.github.io/<repo>/`. On a
phone, open that address in Safari or Chrome and add it to your home screen.

## Built with

Plain HTML, CSS and JavaScript. No framework, no build step, no dependencies,
no CDN. The exercise library comes from
[fitness-app](https://github.com/yahianassef/fitness-app).

## Licence

MIT — see [LICENSE](LICENSE). Take it, change it, make it yours.
