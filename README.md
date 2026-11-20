# d—shboard 🖥

A browser-based start page for your bookmarks. Arrange your favorite sites as visual cards, search the web from the same page, and edit everything in place — no account, no server, no setup.

Your layout is stored in your browser and can be saved to or loaded from a plain `.json` preset file, so it is easy to back up or move to another machine. Built as a lightweight, local-first alternative to cramped bookmark bars and account-bound new-tab pages.

## Why d—shboard?

Bookmark bars are cramped and text-only, and most start pages want an account or a sync service. d—shboard gives you a clean full-page grid of thumbnail cards that you arrange exactly how you like — drag to reorder, edit in place, and keep everything on your own machine.

## Features

- **Visual Link Cards** — Every card has a title, a link, and a thumbnail. Up to 8 cards per row, as many rows as you need.
- **In-Place Edit Mode** — Flip the switch in the header (revealed on hover) to rename cards, change links and image URLs, add or delete cards and rows, and rename the dashboard itself.
- **Drag & Drop Reordering** — Move cards and rows with their grip handles, or use the arrow keys on a focused handle.
- **Smart Thumbnails** — One click fetches the YouTube thumbnail for video links, or the site's favicon for everything else, and caches it locally when the host allows it.
- **Search Rows** — Add a search bar with an animated glow border that searches DuckDuckGo. Align it left, center, or right.
- **Presets** — Save your layout as a `.json` file and import it anywhere. Reset to the starter layout is protected by a two-step confirmation.
- **3D Tilt Cards** — Thumbnails tilt toward your cursor on hover.
- **Responsive & Accessible** — Reflows from 8 columns down to a single column, is fully keyboard operable, announces changes to screen readers, and respects reduced-motion and high-contrast preferences.
- **Auto-Save** — Changes are saved to your browser automatically, with a warning if storage is full.

## Privacy & Architecture

d—shboard is designed with a **local-first** philosophy. Here is exactly what that means for your data:

- **Runs Entirely Client-Side:** Everything happens in your browser. There is no server, no backend, and no account system.
- **Zero Telemetry:** No tracking, no analytics, no update checks. The application does not "phone home."
- **Local Storage Only:** Your layout, dashboard name, and cached thumbnails are saved in your browser's local storage and never leave your machine. Presets are plain files that you save and import yourself.
- **Minimal Network Requests:** No external scripts, fonts, or stylesheets are loaded. The page only contacts other sites when your cards load their images, when you press a card's thumbnail refresh button (YouTube thumbnails or DuckDuckGo favicons), or when you submit a search (DuckDuckGo). No Referer header is sent, and only `http`/`https` links are ever opened.

> **In short:** Your layout never leaves your computer.

## Live Demo

<img width="1920" height="994" alt="preview" src="https://github.com/user-attachments/assets/10d49d59-82c1-4ca6-b2b5-6fb4b6f6d93c" />

Try it directly in your browser: [aquuamon.github.io/D-shboard](https://aquuamon.github.io/D-shboard/)

No installation required — open the page, flip the edit switch, and make it yours. The whole project is a single self-contained file, `dashboard.html`, so you can open it straight from disk or host it on any static site.

## Requirements

- A modern desktop browser (recent Chrome, Edge, Firefox, or Safari)
- Mouse and keyboard recommended for editing — drag-and-drop uses mouse drag events (with a keyboard alternative), while browsing and opening links also works on touch devices

## Instructions

Use d—shboard as your browser's start page:

1. **Download** `dashboard.html` and save it somewhere permanent (for example, your Documents folder). If you move or delete the file, the start page will stop working.
2. **Copy the file's address:** open `dashboard.html` in your browser and copy the address from the address bar (it starts with `file:///`).
3. **Open your browser settings** and set it as your homepage or startup page, then paste the address:
   - **Chrome:** Settings → On startup → *Open a specific page or set of pages* → *Add a new page*. For the Home button, use Settings → Appearance → *Show home button* → *Enter custom web address*.
   - **Edge:** Settings → Start, home, and new tabs → *Open these pages* → *Add a new page*.
   - **Firefox:** Settings → Home → *Homepage and new windows* → *Custom URLs*.
4. **Save** by closing the settings tab. The changes apply automatically.

> **Note:** Browsers don't let you point the *new tab* page at a local file in their built-in settings, so the steps above set your homepage and startup page. To use it for every new tab, install a new-tab redirect extension and paste the same address there (some extensions need file access enabled in their settings). Menu names can vary slightly between browser versions.

## Keybinds

| Key | Action |
|-----|--------|
| `Click` | Open a card's link in a new tab |
| `Enter` | Submit a search (in a search row) |
| `←` / `→` | Move the focused card left/right within its row (edit mode, on its grip) |
| `↑` / `↓` | Move the focused card to the row above/below, or move the row itself when a row grip is focused |
| `Tab` | Move between cards, fields, and grips |

Hover the header (or tab to it) to reveal the edit switch.

In edit mode, use the grab icon (⣿) to move rows and cards into different positions: drag it with the mouse, or focus it and use the arrow keys.

Next to each card's Image URL field, the refresh button (↻) fills in a thumbnail from the card's link: the video thumbnail for YouTube links, or the site's favicon (via DuckDuckGo) for everything else. The image is saved in your browser when the host allows it, otherwise its URL is kept.

## Technology Stack

Built with vanilla **HTML, CSS, and JavaScript** — no frameworks, no build step, no dependencies:
- **DOM APIs** for rendering rows and cards
- **HTML Drag and Drop API** for reordering
- **localStorage** for layout persistence
- **Fetch & File APIs** for thumbnail caching and preset import/export
- **Modern CSS** (custom properties, 3D transforms, conic gradients) for the glass look, tilt cards, and animated search border

## How It Was Built

Part hand-written code, part AI-assisted "vibe coding" development with human design and decisions.

## Donation

Feel free to contribute to this project by leaving a donation at:

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/aquamon)

Thanks!

## License & Attribution

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)**.

**You are free to:**
- ✅ Use the software for personal or educational purposes.
- ✅ Modify, adapt, and fork the code.
- ✅ Share the software with others.

**Conditions:**
- ⚠️ **Attribution**: You must give appropriate credit to the original author.
- ⚠️ **NonCommercial**: You may not use the material for commercial purposes without explicit permission.

> *Note: Commercial use (selling the tool, embedding it in a paid product/service) requires prior authorization from the author.*

For full legal terms, see the [LICENSE](LICENSE) file.

---

**Use at your own responsibility.**
