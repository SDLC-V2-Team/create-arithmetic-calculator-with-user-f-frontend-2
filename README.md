# Arithmetic Calculator

A user-friendly, single-page arithmetic calculator that runs **entirely in the browser** — no server, no build step, no dependencies.

> Architecture reference: **ADR-001 — Use client-side single-page application for calculator**

## Features

- Four basic operations: addition, subtraction, multiplication, division
- Percent (`%`) conversion
- Clear (`AC`) and delete-last (`DEL`)
- Division-by-zero guarded with an `Error` state
- Full keyboard support
- Responsive, accessible (ARIA) dark-themed UI
- **Zero deployment infrastructure** — just open the file

## Tech Stack

| Layer | Technology |
|-------|------------|
| Markup | HTML5 |
| Styling | CSS3 (embedded) |
| Logic | Vanilla JavaScript (ES6, embedded) |

No frameworks, no package manager, no backend — exactly as decided in ADR-001.

## Getting Started

### Option 1 — Open directly

Simply double-click `index.html`, or open it in any modern browser.

### Option 2 — Serve locally (optional)

If you prefer serving over HTTP (e.g. to avoid `file://` quirks), use any static server:

```bash
# Python 3
python3 -m http.server 8080

# Node (npx)
npx serve .
```

Then visit <http://localhost:8080>.

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `0`–`9` | Enter digits |
| `.` | Decimal point |
| `+` `-` `*` `/` | Operators |
| `Enter` or `=` | Compute result |
| `Backspace` | Delete last digit |
| `Escape` | Clear all |
| `%` | Percent |

## Project Structure

```
.
├── index.html      # The entire application (HTML + CSS + JS)
├── README.md       # This file
└── .gitignore
```

## Deployment

Because it is a single static file, this app can be hosted on **any static host**:

- GitHub Pages
- Netlify / Vercel
- Amazon S3 + CloudFront
- Any plain web server

No build pipeline is required.

## License

MIT
