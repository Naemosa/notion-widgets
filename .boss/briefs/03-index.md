# Brief 03 — index.html (new)

**Goal:** a gallery page that shows every widget live and lets the user copy each widget's link to paste into a Notion /embed block.

**Files to write:** `index.html` (new file).

**Interfaces:** links are relative to the page: `new URL(file, location.href).href`.

**Context:** the repo has these widgets (file — French name — short description):
- horloge.html — Horloge — heure et date en cartes roses
- calendrier.html — Calendrier — mois en cours, aujourd'hui mis en avant
- meteo.html — Météo — météo en direct (paramètres `ville`, `lat`, `lon`)
- pomodoro.html — Pomodoro — minuteur travail / pause
- progression.html — Ma progression — année, mois, jour en barres
- humeur.html — Humeur du jour — suivi d'humeur sur 7 jours
- citation.html — Citation du jour — phrase de motivation
- verset.html — Verset du jour — verset biblique (Louis Segond)
- playlist.html — Ma playlist — lecteur Spotify (paramètre `playlist`)
- petales.html — Pluie de pétales — fond animé (paramètre `texte`)

**Rules:**
1. Same visual style as the widgets: background `radial-gradient(circle at 15% 10%,#fff4f8 0,transparent 45%),linear-gradient(160deg,#fde9ef,#f9d3de)`, titles in italic 700 "Playfair Display",Georgia,serif colour `#9b2a4e`, small labels in system-ui uppercase letter-spacing colour `#c2185b`, pink pill buttons like `border:2px solid #ee7f9b;background:#fff7f9;color:#b03a5b;border-radius:999px`.
2. Header: title "Mes widgets Notion ♡" and one line: "Copie un lien, puis dans Notion tape /embed et colle-le."
3. Responsive grid of cards (`repeat(auto-fill,minmax(280px,1fr))`). Each card: name, description, an `<iframe loading="lazy">` preview 220px high with rounded corners and no border, then two buttons: "Copier le lien" (copies the absolute URL with `navigator.clipboard.writeText`, falls back to selecting a hidden input + `document.execCommand("copy")`, then shows "Copié ✓" for 1.5 s) and "Ouvrir" (opens the widget in a new tab).
4. For widgets with parameters, show the parameters under the description in small text, e.g. `?ville=Paris&lat=48.85&lon=2.35`.
5. Page scrolls normally (do not use overflow:hidden on body). 16px side padding on phones, no horizontal scroll.
6. Build the cards from one JS array, not hand-written HTML repeated 10 times.
7. No libraries, no external files. French text.

**Done when:** the boss opens it in headless Chromium, counts 10 cards and 10 iframes, and clicks one "Copier le lien" without a JS error.
