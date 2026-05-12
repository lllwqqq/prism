# Prism

**Your tabs, refracted.**

Prism replaces your Chrome new tab page with a glassmorphism dashboard that groups everything you have open by domain. Homepages (Gmail, X, LinkedIn, YouTube, GitHub) get their own card. Close tabs with a satisfying swoosh + confetti burst.

No server. No account. No data leaves your machine.

---

## Features

| Feature | Description |
|---------|-------------|
| Domain grouping | All open tabs organized by domain on a clean grid |
| Homepages card | Gmail inbox, X home, YouTube, LinkedIn, GitHub in one group |
| Swoosh + confetti | Close tabs with animated sound and particle burst |
| Duplicate detection | Same page open twice? Flagged and one-click cleanup |
| Cross-window jump | Click any tab title to switch to it, even across windows |
| Save for later | Bookmark tabs to a checklist before closing them |
| Auto-refresh | Dashboard updates in real-time when tabs change |
| Localhost ports | Port numbers shown next to each local dev tab |
| Expandable cards | First 8 tabs shown, click "+N more" to expand |
| 100% local | Your data never leaves your machine |

---

## Install

### Quick setup

1. Open Chrome and go to `chrome://extensions`
2. Enable **Developer mode** (top-right toggle)
3. Click **Load unpacked**
4. Select the `extension/` folder from this project
5. Open a new tab — you'll see Prism

> Setup takes about 1 minute. No server, no Node.js, no npm.

---

## How it works

```
New tab
  → Prism shows all open tabs grouped by domain
  → Homepages get their own group at the top
  → Click any tab title to jump to it
  → Close groups when you're done (swoosh + confetti)
  → Save tabs for later before closing them
```

Everything runs inside the Chrome extension. Saved tabs are stored in `chrome.storage.local`.

---

## Tech

| Layer | Technology |
|-------|-----------|
| Extension | Chrome Manifest V3 |
| Storage | chrome.storage.local |
| Sound | Web Audio API (synthesized) |
| Animation | CSS transitions + JS confetti particles |

---

## License

MIT — Author: Lee
