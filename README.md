# Cynthia's quest

Five files. Keep them all in the same folder, with no sub-folders and no renaming.

```
index.html    the forest, portal, passcode, trivia, secret question, hub
mail.html     the letter
song.html     the music player
flower.html   build a bouquet
colour.html   colour in the photos
```

`index.html` must keep that name — GitHub Pages looks for it, and every "HUB" button points back to it.

## Putting it on GitHub Pages

1. Make a new repository on GitHub (public).
2. Upload all five files to the root of it, not inside a folder.
3. Repository **Settings** → **Pages** → under *Build and deployment*, set **Source** to *Deploy from a branch*, branch **main**, folder **/ (root)**. Save.
4. Wait a minute or two, then open `https://<your-username>.github.io/<repo-name>/`.

That address is what you send her. It works on phones as well as laptops.

## Checking it locally first

Opening the files straight from the folder works for everything **except the songs** — YouTube refuses to play inside a `file://` page. To test that part before you publish, open a terminal in the folder and run:

```
python3 -m http.server
```

then visit `http://localhost:8000/`.

## Things you might want to edit

| What | Where |
|---|---|
| The passcode (2409) | `index.html`, search for `PASSCODE` |
| Trivia questions and answers | `index.html`, search for `QUESTIONS` |
| The letter | `mail.html`, search for `Dear Cynthia` |
| Songs, start times, snippet lengths | `song.html`, search for `const SONGS` |

## Shortcuts for testing

Add these to the end of the address to skip ahead in `index.html`:

- `#quest` — straight to the trivia
- `#secret` — straight to the secret question
- `#hub` — straight to the hub

## Notes

- Progress in the colouring page and the sound volume are saved in her browser, so they survive a refresh.
- The sound button sits in the top right of every page and its setting carries across all of them.
- Music starts after her first tap; browsers block audio before that.
