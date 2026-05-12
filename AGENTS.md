# AGENTS.md — Prism: Setup & Onboarding Guide

You're installing **Prism** for the user. Your job is not just to set it up — it's to get them excited about using it.

---

## Step 0 — Introduce the product

Before doing anything technical, tell the user what they're about to get:

> **Prism** replaces your new tab page with a glassmorphism dashboard of everything you have open, grouped by domain.
>
> Highlights:
> - **See all open tabs at a glance** — grouped by domain on a clean grid
> - **Homepages card** — Gmail, X, LinkedIn, YouTube, GitHub in one place
> - **Swoosh + confetti** — satisfying close animation with sound
> - **Duplicate detection** — same page open twice? One-click cleanup
> - **Cross-window jump** — click any tab title to switch to it
> - **Save for later** — bookmark tabs to a checklist before closing
> - **Auto-refresh** — dashboard updates in real-time
> - **100% local** — no server, no accounts, no data sent anywhere
>
> It's a Chrome extension. Setup takes about 1 minute.

---

## Step 1 — Get the project

Open the project folder in your terminal (the folder containing `extension/`).

```bash
cd /path/to/prism
```

---

## Step 2 — Install the Chrome extension

This is the only step that requires manual action from the user.

**Print** the full path to the `extension/` folder:

```bash
echo "Extension folder: $(cd extension && pwd)"
```

**Copy** the path to clipboard:

- macOS: `cd extension && pwd | pbcopy && echo "Path copied to clipboard"`
- Linux: `cd extension && pwd | xclip -selection clipboard 2>/dev/null || echo "Path: $(pwd)"`
- Windows: `cd extension && echo %CD% | clip`

**Open** the extensions page:

```bash
open "chrome://extensions"
```

**Walk the user through it:**

> I've copied the extension folder path to your clipboard. Now:
>
> 1. On Chrome's extensions page, toggle on **Developer mode** (top-right switch).
> 2. Click **"Load unpacked"** (top-left).
> 3. Press **Cmd+Shift+G** (Mac) or **Ctrl+L** (Windows/Linux), paste the path, and press Enter.
> 4. Click **"Select"** — the extension will install.
>
> You should see "Prism" in your extensions list.

**Fallback** — open the folder in Finder/Explorer:

- macOS: `open extension/`
- Linux: `xdg-open extension/`
- Windows: `explorer extension\\`

---

## Step 3 — Show them around

> You're all set! Open a **new tab** and you'll see Prism.
>
> Quick guide:
> 1. **Tabs grouped by domain** in a grid layout
> 2. **Homepages** (Gmail, X, YouTube, etc.) in their own group at the top
> 3. **Click any tab title** to jump directly to it
> 4. **Click X** to close a single tab (swoosh + confetti)
> 5. **"Close all N tabs"** closes an entire domain group
> 6. **Duplicate tabs** show a purple "(2x)" badge — click "Close duplicates" to keep one
> 7. **Save for later** — click the bookmark icon; saved tabs appear in the sidebar
> 8. **Auto-refreshes** when tabs change — no manual refresh needed
>
> No server, no config. It just works.

---

## Key facts

- Pure Chrome extension. No server, no Node.js, no npm.
- Saved tabs stored in `chrome.storage.local` (persists across sessions).
- 100% local. No data sent to any external service.
- To update: pull the latest changes, then reload the extension in `chrome://extensions`.
- Author: Lee
