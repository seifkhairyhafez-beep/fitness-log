# Log. – Training Ledger

A small training log I built to plan and track my weekly workouts and swim sessions. It runs as a Progressive Web App, so it can be installed on a phone and works offline.

## Features

- **This Week:** a 7-day plan with session types (push, legs, swim, rest …), check-off per day and a progress ring
- **Session logger:** distance, active time, average heart rate and calories per session, plus notes
- **Swim plans:** two structured pool sessions with sets and drills
- **History:** all logged sessions with edit and delete, personal bests and weekly and monthly totals
- Light and dark mode (follows the system setting)

## How it works

- Everything is in one `index.html` (HTML, CSS and plain JavaScript, no framework, no build step)
- Data is stored in the browser with `localStorage` (`fitlog_week_v2` for the current week, `fitlog_history_v1` for logged sessions). Nothing is sent to a server.
- `sw.js` is a service worker that caches the app so it opens without a connection. `manifest.json` makes it installable.

## Run it

Open `index.html` in a browser. For the offline and install features it needs to be served over `localhost` or HTTPS, for example:

```
python -m http.server 8000
```

Then open http://localhost:8000.
