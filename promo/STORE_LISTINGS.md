# Flipp's Favorites — Store Listings

> Source-of-truth copy for all three storefronts. Current as of **v2.3.0**.
> Headline feature since v2.0: **Workspaces** — turn any bookmark folder into its own isolated, themed dashboard.
>
> Where a store differs (character limits, category names, fields), it is called out under that store's heading. Shared long-form copy lives once in the **Shared description blocks** section at the bottom; each store points to it.

---

## Brand & naming

| Field | Value | Notes |
| --- | --- | --- |
| Product name | **Flipp's Favorites** | Always with the apostrophe. |
| Manifest name | `Flipp's Favorites - New Tab Workspaces` | 38 chars — safe everywhere. |
| Tagline | *Your bookmarks, reimagined as a workspace.* | |
| Website | https://www.flippflix.com | |
| Support / issues | https://github.com/Flippeey/flipps-favorites/issues | |

---

## 1. Chrome Web Store

| Field | Limit | Value |
| --- | --- | --- |
| **Name** | ≤ 45 chars | `Flipp's Favorites - New Tab Workspaces` (38 chars) |
| **Short description** | ≤ 132 chars | `Turn your new tab into a fast, visual bookmark workspace — folders, search, custom icons, themes, and a dock. Zero setup.` (120 chars) |
| **Category** | — | **Workflow & Planning** (fallback: Tools) |
| **Language** | — | English (US) |
| **Detailed description** | ≤ 16,000 chars | → use **[Long description]** block below |

**Keywords / search terms** (Chrome has no dedicated keyword field — weave these naturally into the description; these are the terms to optimise for):
`new tab`, `bookmarks`, `bookmark manager`, `start page`, `dashboard`, `workspaces`, `productivity`, `speed dial`, `favorites`, `homepage`, `dock`, `private`, `no tracking`, `customizable new tab`

---

## 2. Microsoft Edge Add-ons

Edge mirrors the Chrome build (same MV3 package). Copy is identical except where noted.

| Field | Value |
| --- | --- |
| **Name** | `Flipp's Favorites - New Tab Workspaces` |
| **Short description** | Same as Chrome short description (Edge allows up to ~200 chars; the Chrome line is fine). |
| **Category** | **Productivity** |
| **Detailed description** | → use **[Long description]** block below |
| **Search terms** | Edge provides up to **7** keyword slots. Use: `new tab`, `bookmarks`, `workspaces`, `dashboard`, `productivity`, `start page`, `bookmark manager` |

> **Edge note:** the listing requires a privacy policy URL. Point it at the privacy section of https://www.flippflix.com (or a dedicated `/privacy` page). The answer to data-collection questions is **"does not collect"** across the board.

---

## 3. Firefox Add-ons (AMO)

| Field | Limit | Value |
| --- | --- | --- |
| **Name** | ≤ 50 chars | `Flipp's Favorites - New Tab Workspaces` |
| **Summary** | ≤ 250 chars | `Replace your new tab with a fast, visual bookmark workspace. Your existing bookmarks appear instantly — no import. Turn any folder into its own themed Workspace, search everything live, customise icons and layout. 100% local, no tracking.` (236 chars) |
| **Categories** (pick up to 2) | — | **Bookmarks**, **Tabs** |
| **Description** | — | → use **[Long description]** block below |
| **Tags** (up to ~10) | — | `new-tab`, `bookmarks`, `workspaces`, `dashboard`, `productivity`, `start-page`, `dock`, `privacy`, `customization`, `speed-dial` |

> **Firefox notes:**
> - The Firefox build uses a background **page** (not a service worker) and requires Firefox **140+** (Android **142+**). State minimum version in the listing if asked.
> - AMO requires a clear answer on data collection: declare **none** (matches `data_collection_permissions.required = ["none"]` in the manifest).
> - `browser_specific_settings.gecko.id` is `com.flipps-favorites@flippflix.com`.

---

# Shared description blocks

## [Long description]

**Flipp's Favorites — your bookmarks, reimagined as a workspace.**

You open a new tab dozens of times a day. Flipp's Favorites turns that blank page into the most useful screen in your browser: a fast, visual dashboard built directly on top of the bookmarks you already have. Install it and everything's already there — no imports, no CSV files, no accounts, no starting from scratch.

### ⭐ Workspaces — one browser, many dashboards

The headline feature. Turn **any bookmark folder into its own isolated Workspace** — a self-contained dashboard with its own theme, accent colour, wallpaper, layout, and dock. Keep a focused space for work, another for research, another for side projects or clients. Switch between them in a single click (or Ctrl/Cmd + 1–9), drag a bookmark onto a workspace tab to move it, and reorder tabs however you like. Up to nine Workspaces, zero mental overhead.

### What it does

Flipp's Favorites replaces your default new-tab page with a customisable grid of your bookmark folders. Favicons load automatically so you can spot sites at a glance. A live search bar filters everything as you type. Drag bookmarks and folders into any order, resize sections, drop shortcuts into the dock — all without ever leaving the tab.

### Features

• **Workspaces** — turn any folder into an isolated, themed dashboard and switch contexts instantly.
• **Zero setup** — your existing browser bookmarks appear the moment you install. No imports, no manual entry, no accounts.
• **Live fuzzy search** — filter across your entire bookmark library from the hero search bar. Results update as you type and understand your folder structure.
• **The Dock** — a quick-access strip for your most-used folders and sites, always a click away. Always-visible, hover-only, or hidden — your call.
• **Custom icons** — automatic favicon detection for every site, with a 30-day smart cache. Override any icon with a custom image, a URL, or pick one from the built-in icon search.
• **Flexible layouts** — Compact, Balanced, Spacious, and Presentation density presets, or fine-tune columns, gaps, and tile sizes until it feels right.
• **Beautiful backgrounds** — solid colour, rich gradients (aurora, mesh, vignette, and more), or your own wallpaper with opacity, fit, and position controls.
• **Themes** — light, dark, or system-auto, with 10 hand-crafted accent colours and a custom colour picker — set per Workspace.
• **Drag and drop everywhere** — reorder bookmarks, drop into folders, move items between Workspaces, and rearrange layout sections live.
• **Multi-select** — marquee or Ctrl/Cmd-click to select many bookmarks at once, then cut, copy, paste, or bulk-delete with confirmation.
• **Inline editing & folder management** — rename, retag, create, and delete folders right from the page. No browser bookmark manager required.
• **Import and export** — back up your full settings and icon overrides as a single JSON file. Restore on any device or browser in seconds.
• **Completely private** — everything is stored locally in your browser. No cloud sync, no accounts, no tracking, no analytics, no ads.

### Privacy

Flipp's Favorites has no backend and no servers. Your bookmarks and preferences never leave your browser. The only network requests are to fetch site icons — and only the hostname of a bookmark is ever sent, to icon services (Icon Horse, DuckDuckGo, standard favicon endpoints). No data is collected, stored remotely, or shared. No telemetry. No analytics.

### Free, no strings attached

Flipp's Favorites is free, with no paid tiers, no feature gates, and no ads — now or in the future.

### Getting started

Install the extension and open a new tab. The short onboarding wizard scans your bookmarks and suggests Workspaces to get you set up in under a minute. Your sites are already waiting for you.

---

## Required assets checklist (per store)

| Asset | Chrome | Edge | Firefox |
| --- | --- | --- | --- |
| Icon (128px) | ✓ | ✓ | ✓ (uses manifest icons) |
| Small promo tile (440×280) | ✓ | optional | — |
| Marquee promo (1400×560) | optional | optional | — |
| Screenshots (1280×800 or 1920×1080) | 1–5 | 1–10 | up to 10 |
| Privacy policy URL | required | required | required |

Screenshots already generated (gitignored) live in `flipps-favorites/promo/screenshots/{light,dark}/` at both 1280×800 and 1920×1080. Recommended order for all stores: **02-workspaces → 01-hero → 04-search-results → 03-folder-open → 05-settings-appearance**.
