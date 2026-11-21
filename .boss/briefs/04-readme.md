# Brief 04 — README.md

**Goal:** a README that lists every widget, its URL parameters, and how to add one to Notion.

**Files to write:** `README.md` (replace the current 2-line file).

**Context:** current README:
```
# notion-widgets
Widgets roses pour mon Notion
```
Widgets: see the list in `.boss/briefs/03-index.md` (same names and descriptions). There is also a new `index.html` gallery page listing all widgets with a "Copier le lien" button.

**Rules:**
1. In French. Keep the title `# notion-widgets` and the line "Widgets roses pour mon Notion".
2. Section "Ajouter un widget dans Notion": host the repo with GitHub Pages (Settings → Pages → branch `main`, folder `/`), open the gallery `https://<utilisateur>.github.io/notion-widgets/`, copy a link, in Notion type `/embed`, paste, resize the block. Use the placeholder `<utilisateur>` — do not invent a username.
3. Section "Les widgets": a table with columns Widget | Fichier | Paramètres.
4. Section "Paramètres" with examples:
   - `meteo.html?ville=Paris&lat=48.8566&lon=2.3522` (default: Jarry · Guadeloupe)
   - `playlist.html?playlist=<id de la playlist Spotify>` — the id is the part after `/playlist/` in the Spotify share link
   - `petales.html?texte=Bonne%20journée` (spaces written `%20`)
5. Short note: humeur and pomodoro save their data in the browser (localStorage), so it stays on that device.
6. Under 70 lines. Do not touch any other file.

**Done when:** the boss reads it and checks every file name in it exists in the repo.
