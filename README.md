# dienst-db

Small connection search (train journeys: times, platforms, transfers, delays) for a private, single-user Telegram bot.
It queries the public [Transitous](https://transitous.org) API (MOTIS 2), lightly: at most 4 requests per minute and
100 per day, answers cached for 2 minutes. No prices, no tickets.

- Data: [Transitous](https://transitous.org/sources/), [OpenStreetMap](https://www.openstreetmap.org/copyright)
- Needs Node 18+ and `luxon` (see `package.json`).
- Usage: `node dienst-db.mjs verbindung --von "Berlin Hbf" --nach "München Hbf" --datum 2026-11-08 --zeit 08:00 --ab`
- Output: one JSON object built from an allowlist of fields.

License: MIT
