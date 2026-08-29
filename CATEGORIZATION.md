# Categorization & Star Pattern

This document is the **single source of truth** for how apps are organized and
marked in this bucket's `README.md`. It applies to every manifest shipped in
`bucket/`.

The `README.md` is generated from `build-readme.ps1`. The rules below are what
that generator (and any manual edit) must follow. When this document and the
generated output disagree, fix the **output** to match this document.

## 1. Categories

Top-level categories (`###` headings) group apps by their **primary domain**.
There are no subcategories — each category is a single flat table. The fixed set is:

| Category | Scope |
| --- | --- |
| Anime, Manga & Comics | Anime/manga **video** streamers, players, tracking, cataloging, manga/comic **readers** and manga tools/conversion |
| Visual Novel & Text Hooking | VN text hookers, popup dictionaries |
| Language & Dictionaries | Language learning / dictionary tools |
| Music | Music players, trackers/synthesizers, audio tagging tools |
| Gaming & Modding | Storefronts, launchers, Steam tools, modding, Minecraft |
| Emulation & Homebrew | Game emulators and console homebrew tools |
| Media Players & Servers | General media players / media servers (Emby, Jellyfin clients) |
| Subtitles | Subtitle search / edit / conversion tools |
| Downloaders & Automation | Downloaders (manga & novels, fan content & media, torrent automation, stream downloaders) |
| Chinese Apps | Apps whose **primary audience or service is Chinese-language** (Bilibili clients, Chinese subtitle tools, Chinese-service downloaders/readers, Chinese media plugins, etc.) |
| Utilities & Misc | General-purpose tools with no weeb-specific primary function |
| Retro & Geeky Hobbies | IRC, retro computing, electronics sims, etc. |

`Chinese Apps` is a deliberate **locale/origin** grouping: apps that mainly
target Chinese services or audiences are filed there even when a functional
category would also fit (e.g. `chinesesubfinder`, `ChineseSubtitleConversionTool`,
`bilibili-tui`). All other categories are grouped by primary function.

## 2. Assignment rules

- **Each manifest is listed exactly once**, in the single most appropriate table.
- Assign by *what the app primarily does*, preferring function over origin
  (except for the `Chinese Apps` locale grouping above):
  - Anime/manga **video** streamers & players, trackers, cataloging, manga/comic
    **readers**, manga tools → **Anime, Manga & Comics**
  - Subtitle **search / edit / convert** tools → **Subtitles**
  - Downloaders → **Downloaders & Automation**
  - General-purpose tools with no weeb-specific primary function → **Utilities & Misc**
- **Canary / pre-release / server variants** are listed in the **same table**
  as their stable app. The display name is suffixed with ` (canary)` or
  ` (server)` as appropriate (e.g. `Seanime (canary)`, `Seanime Server`).

## 3. Sorting (within every table)

1. **Starred** apps first, sorted alphabetically (case-insensitive).
2. Then the **remaining** apps, sorted alphabetically (case-insensitive).

The star mark never changes an app's alphabetical slot among the other
starred apps; it only floats the starred group to the top of the table.

## 4. Star (renowned) mark — `⭐` (U+2B50)

- The star marks apps that are the **de-facto standard or widely renowned**
  in their domain (large, cross-community user base, actively maintained).
- It is a **curated "recommended" badge** set by maintainer judgment.
  It is **not** automatic (not derived from download counts).
- **Canary / pre-release / server builds are not starred.**
- The mark is appended to the app name inside the table link:
  `[App Name ⭐](homepage)`.

## 5. Adding a new app (maintainer checklist)

1. Pick the one table from §1/§2 that matches the app's primary function
   (or locale, for `Chinese Apps`).
2. Add the app's name to that table's list, sorted per §3.
3. If the display name differs from the manifest filename, register the
   mapping in the generator's `$disp` table and a purpose string in `$orig`.
4. If the app qualifies under §4, add its manifest name to the `$star` list.
5. Regenerate `README.md` and run `bin\test.ps1` (expect all tests to pass).

## 6. Known deviations to resolve

These were found during review and should be reconciled with this pattern:

- `seanime-denshi-canary`, `seanime-server`, `seanime-server-canary` exist in
  `bucket/` but are **not yet listed** in `README.md`.
