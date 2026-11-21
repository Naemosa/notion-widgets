# PLAN — Améliorer les widgets Notion

Builder: Claude Haiku (no GPU here, so qwen3.8:27b cannot run; see "No local model").
Boss: Claude. The boss writes only inside `.boss/`.

## Tasks

| # | Task | File(s) | Depends on |
|---|------|---------|------------|
| 01 | Pomodoro: drift-proof timer + daily count saved | `pomodoro.html` | — |
| 02 | Calendrier: back to today + mouse wheel / swipe | `calendrier.html` | — |
| 03 | Galerie: page listing every widget with a "copy link" button | `index.html` | — |
| 04 | README: widget list, URL parameters, how to embed in Notion | `README.md` | — |

All tasks are independent and can run in parallel.

## Frozen interfaces
- Existing widget file names and URL parameters do not change:
  - `meteo.html?ville=…&lat=…&lon=…`
  - `playlist.html?playlist=<Spotify playlist id>`
  - `petales.html?texte=…`
- Shared look: pink palette (`#fde9ef`, `#f9d3de`, `#ec6f90`, `#c2185b`, `#9b2a4e`, `#6e1532`),
  "Playfair Display",Georgia,serif for titles, system-ui for small labels, ♡ ✿ ✦ ornaments, French text.
- localStorage is always wrapped in try/catch (the existing `lire`/`ecrire` pattern in humeur.html).
- No external scripts or libraries. One self-contained HTML file per widget.
