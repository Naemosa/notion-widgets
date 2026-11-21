# Brief 01 — pomodoro.html

**Goal:** make the Pomodoro timer exact even when the Notion tab is in the background, and keep the day's session count after a reload.

**Files to write:** `pomodoro.html` (edit the existing file; keep everything else).

**Interfaces:** no URL parameters. Same HTML structure, same ids (`t`, `nom`, `prog`, `go`, `raz`, `compte`), same CSS look.

**Context:** read the current `pomodoro.html` in the repo root before editing.

**Rules:**
1. Timer: when started, store `fin = Date.now() + reste*1000`. Each tick (every 250 ms is fine) compute `reste = Math.max(0, Math.ceil((fin - Date.now())/1000))`. Pause keeps the remaining seconds; resume sets a new `fin`. No more `reste--`.
2. When it reaches 0: stop, play the existing `son()`, and if the active mode is "Travail 25", increment the count.
3. Count is saved per day in localStorage under the key `pomodoro-AAAA-M-J` (same format as humeur.html: `getFullYear()+"-"+(getMonth()+1)+"-"+getDate()`). Read it at load. Wrap every localStorage access in try/catch, like `lire`/`ecrire` in humeur.html.
4. Show the remaining time in the page title while running (`"12:34 · Pomodoro"`), and restore `"Pomodoro"` when stopped.
5. Keep the French text and grammar ("1 séance aujourd'hui", "2 séances aujourd'hui"; 0 → "0 séance aujourd'hui").
6. Do not add libraries. Do not touch any other file.

**Done when:** `node -e` cannot load HTML, so the boss will extract the `<script>` and run `node --check`, then load the page in headless Chromium, click Lancer, and check the time goes down and the title changes.
