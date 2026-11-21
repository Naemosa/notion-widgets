# notion-widgets
Widgets roses pour mon Notion

## Les widgets

| Widget | Fichier | Paramètres |
|---|---|---|
| Horloge | `horloge.html` | — |
| Calendrier | `calendrier.html` | — |
| Météo | `meteo.html` | `ville`, `lat`, `lon` |
| Pomodoro | `pomodoro.html` | — |
| Ma progression | `progression.html` | — |
| Humeur du jour | `humeur.html` | — |
| Citation du jour | `citation.html` | — |
| Verset du jour | `verset.html` | — |
| Ma playlist | `playlist.html` | `playlist` |
| Pluie de pétales | `petales.html` | `texte` |

## Ajouter un widget dans Notion

1. Héberger le dépôt avec GitHub Pages : dans le dépôt, Settings → Pages, choisir la branche `main` et le dossier `/`.
2. Ouvrir la galerie : `https://<utilisateur>.github.io/notion-widgets/`.
3. Cliquer sur « Copier le lien » du widget voulu.
4. Dans Notion, taper `/embed`, coller le lien, puis redimensionner le bloc.

## Paramètres

Les paramètres s'ajoutent à la fin du lien, après `?`, séparés par `&`.

- `meteo.html?ville=Paris&lat=48.8566&lon=2.3522` (par défaut : Jarry · Guadeloupe)
- `playlist.html?playlist=<id de la playlist Spotify>` : l'id est la partie après `/playlist/` dans le lien de partage Spotify
- `petales.html?texte=Bonne%20journée` (les espaces s'écrivent `%20`)

## Données

Les widgets Humeur et Pomodoro enregistrent leurs données dans le navigateur (localStorage) : elles restent donc sur l'appareil utilisé.
