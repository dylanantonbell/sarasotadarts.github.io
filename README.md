# sarasotadarts.github.io
website for promoting darts in the Sarasota area (TDLS, MDLS, events, venues, etc.)

## Adding New Images

Images are organized by purpose inside the `img` folder:

- `img/blind-draws/`
- `img/tdls-teams/`
- `img/mdls-teams/`
- `img/venues/`
- `img/state-team/`
- `img/logos/`

The gallery page is driven from one file: `gallery-data.json`.

To add a new gallery image:

1. Add the image file to the correct folder.
2. Open `gallery-data.json`.
3. Add a new object to the JSON array.
4. Use one of these categories exactly:
   - `Blind Draws`
   - `TDLS Teams`
   - `MDLS Teams`
   - `Venues`
   - `State Team`
   - `Logos`
5. Commit and push the changes:

```bash
git add .
git commit -m "Add new gallery images"
git push
```

Future AI workflow:

When you upload a new image and say something like `Add this image to the TDLS Teams gallery`, the AI only needs to:

1. Rename the image with a clear filename, such as `tdls-summer-2026-team.jpg`.
2. Save it into the matching folder, such as `img/tdls-teams/`.
3. Add one new object to `gallery-data.json` with the title, category, image path, and caption.

Example entries:

```json
[
  {
    "title": "June 2026 Blind Draw Winners",
    "category": "Blind Draws",
    "image": "img/blind-draws/june-2026-winners.jpg",
    "caption": "Blind Draw winners from June 2026."
  },
  {
    "title": "TDLS Summer 2026 Team",
    "category": "TDLS Teams",
    "image": "img/tdls-teams/tdls-summer-2026-team.jpg",
    "caption": "TDLS team photo from the Summer 2026 season."
  },
  {
    "title": "MDLS Spring 2026 Team",
    "category": "MDLS Teams",
    "image": "img/mdls-teams/mdls-spring-2026-team.jpg",
    "caption": "MDLS team photo from the Spring 2026 season."
  },
  {
    "title": "8-Ball Lounge Dart Area",
    "category": "Venues",
    "image": "img/venues/8ball-dart-area.jpg",
    "caption": "Dart area at 8-Ball Lounge."
  },
  {
    "title": "TDLS State Team 2026",
    "category": "State Team",
    "image": "img/state-team/tdls-state-team-2026.jpg",
    "caption": "TDLS State Team photo from 2026."
  }
]
```
