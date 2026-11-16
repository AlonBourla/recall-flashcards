# Recall — Anki-inspired offline flashcards

Recall is a small installable web app for iPhone. It runs in Safari, can be added to the Home Screen, and stores cards in the browser on the device. Once installed and cached, the core app works offline.

## Included
- Decks and flashcards (front/back)
- Daily due-card review
- Four review ratings: Again, Hard, Good, Easy
- Simple interval-based spaced repetition
- Tags
- CSV import/export and full JSON backup/restore
- Local browser storage; no account or server database

This is an original Anki-inspired starter app, not an exact copy of Anki. It does not include Anki's FSRS scheduler, AnkiWeb sync, desktop add-ons, media/audio cards, shared decks, or cross-device sync.

## Install on iPhone (recommended: GitHub Pages)
iOS only allows a service worker and reliable offline installation from a secure HTTPS website (or localhost). For the simplest no-cost route:

1. On a computer, sign in to GitHub and create a new **public** repository, e.g. `recall-flashcards`.
2. Unzip this project. Upload **all files inside the folder** to the repository's top level. Make sure `index.html` is at the top level, not inside another folder.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
5. Wait for GitHub Pages to publish. It will show an HTTPS address similar to `https://YOUR-USERNAME.github.io/recall-flashcards/`.
6. Open that HTTPS address in **Safari on your iPhone** (not an in-app browser).
7. Tap **Share** → **Add to Home Screen** → **Add**.
8. Launch **Recall** from the new Home Screen icon. Open it once while online so the offline files are cached. Then test by enabling Airplane Mode and reopening it.

## Use
1. Open **Decks** and create a deck (for example, “Hebrew vocabulary”).
2. Open **Add cards**, choose the deck, and enter the prompt on the front and answer on the back.
3. Open **Study**. Tap **Show answer**, then rate how well you remembered:
   - **Again**: you did not remember; review tomorrow.
   - **Hard**: remembered with difficulty; a short interval.
   - **Good**: remembered; a longer interval.
   - **Easy**: very easy; the longest interval.
4. The next due date is calculated automatically. Study cards marked due today.
5. Back up regularly using **Import / export → Export backup**. Keep the JSON file in Files or iCloud Drive.

## Import CSV
Use columns in this order: `Deck,Front,Back,Tags`. Tags are separated by semicolons. Save as UTF-8 CSV. Example:

```csv
Deck,Front,Back,Tags
Hebrew,אָחוּ,brother; kinship,noun
Hebrew,השתאות,astonishment; wonder,abstract
```

## Important data note
Cards are stored in Safari's local website storage on that iPhone. Clearing Safari website data, deleting browser data, or removing site data can erase the collection. Export JSON backups regularly. GitHub Pages hosts the app files; it does not receive your flashcard contents through this app.

## Updating the app
Upload the new app files to the same GitHub repository. Close and reopen Recall while online. If an old version remains, fully close the Home Screen app and reopen it after a short wait.
