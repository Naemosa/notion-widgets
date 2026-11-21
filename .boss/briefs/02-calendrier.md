# Brief 02 — calendrier.html

**Goal:** make it easy to come back to the current month and to change months.

**Files to write:** `calendrier.html` (edit the existing file; keep everything else).

**Interfaces:** same ids (`prec`, `suiv`, `titre`, `grille`, `pied`), same look.

**Context:** read the current `calendrier.html` in the repo root before editing.

**Rules:**
1. Clicking the month title (`#titre`) goes back to the current month. Give it `cursor:pointer`, `title="Revenir à aujourd'hui"`, and make it a `<button>`-like element reachable by keyboard (role="button", tabindex="0", Enter/Space activate it). Keep its current font style.
2. Keyboard: ArrowLeft / ArrowRight on the document change month.
3. Touch: a horizontal swipe of more than 40 px on `.grille` changes month (left swipe → next month).
4. Refresh at midnight: every minute, if the date changed since load, update the "today" highlight and footer (redraw with the new date).
5. Refactor the month change into one function `change(delta)` used by the buttons, keys and swipe.
6. No libraries. Do not touch any other file. Keep French text.

**Done when:** the boss runs `node --check` on the extracted script and, in headless Chromium, clicks ›, then the title, and checks the title is back to the current month.
