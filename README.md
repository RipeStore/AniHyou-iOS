# AniHyou iOS Builder

Automated CI/CD builder and release pipeline for [AniHyou iOS](https://github.com/axiel7/AniHyou-iOS) — an open-source, modern AniList client for iOS and watchOS.

This build is distributed by a third party not related to axiel7/anihyou

---

## 📱 About AniHyou

AniHyou is a native, feature-rich AniList client built with Swift and SwiftUI.

### Features
- ⌚️ **watchOS Support** — Native companion app for Apple Watch
- 📅 **Air Schedule & Calendar** — Airing soon, seasonal animes, and weekly calendar
- 🔥 **Trending & Discover** — Explore trending anime/manga, charts (top & popular)
- 📖 **Comprehensive Details** — Anime/Manga info, tags, characters, staff, recommendations, relations, reviews, stats
- 📝 **List Management** — Manage Anime/Manga lists (status, progress, score, dates, repeat)
- 🔍 **Global Search** — Search animes, mangas, characters, staff, studios, and users
- 👤 **User Profiles** — User activity feeds, bios, and favorites
- 🧩 **Widgets** — Airing anime widgets for iOS Home Screen & Lock Screen

---

## 🚀 Automated Builds & Releases

This repository runs an automated GitHub Actions pipeline:
- ⏰ **Scheduled Runs:** Automatically queries the official Apple App Store API for published AniHyou releases (e.g. `1.8.7`), resolves the corresponding upstream commit (`build: <version>`), and builds when a new release drops.
- ⚙️ **Manual Dispatch (`workflow_dispatch`):** Build any branch (`main`), commit SHA, tag, or force rebuild on demand.
- 📦 **Unsigned IPAs:** Compiles with Xcode, strips signature constraints, and packages ready-to-sideload `.ipa` releases.

### Workflow Inputs
- `target`: Upstream Tag, Branch, or Commit SHA (leave empty to auto-detect latest App Store release).
- `force_rebuild`: Force rebuild even if a release for that target already exists.
- `is_prerelease`: Mark published release as pre-release.
- `anilist_client_id`: Optional custom AniList OAuth Client ID (or set `ANILIST_CLIENT_ID` repo secret).
- `mal_client_id`: Optional custom MyAnimeList Client ID (or set `MAL_CLIENT_ID` repo secret).

---

## 🖼️ Screenshots

| | | |
|:---:|:---:|:---:|
| <img src="screenshots/screenshot_01.webp" width="100%"/> | <img src="screenshots/screenshot_02.webp" width="100%"/> | <img src="screenshots/screenshot_03.webp" width="100%"/> |

---

## 🔗 Links & Upstream Repository

- **Upstream Repository:** [https://github.com/axiel7/AniHyou-iOS](https://github.com/axiel7/AniHyou-iOS)
- **App Store:** [https://apps.apple.com/us/app/anihyou/id1635777325](https://apps.apple.com/us/app/anihyou/id1635777325)
- **Official TestFlight:** [https://testflight.apple.com/join/Om3OIlKd](https://testflight.apple.com/join/Om3OIlKd)
- **Upstream Developer (Axel Lopez):** [axiel7](https://github.com/axiel7)
