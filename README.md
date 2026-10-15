# Beatz

A Spotify-style music player prototype that runs entirely in the browser as a single `index.html` file.

Every song is composed live with the Web Audio API, so there are no audio files and nothing to license.

## Features

- Home, Search, Library and Queue pages
- Curated playlists, artist and genre pages, and Liked Songs
- Your own playlists: create, add songs, remove songs, delete
- Play/pause, next/previous, seek, shuffle, repeat (all or one), volume
- Full-screen Now Playing view with a live audio visualizer, tempo and key
- On phones, a bottom tab bar with a colour for each section: Home, Search, Library and Queue

- Night-stage theme with a live background that moves to the music: spinning vinyl with sound bars, beat rings, flowing waves, floating notes and an equalizer skyline (turn it off in Library → Visuals)
- Your own songs: add audio files from your device, or put MP3s in the `songs` folder

Likes, playlists and uploaded songs are saved in your browser.

## Beatz Originals

The `songs` folder ships with nine original songs, including four techno tracks, made for this app. They are public domain (CC0), so anyone can play, share or reuse them. See `songs/LICENSE.txt`.

| Song | Style | Length |
| --- | --- | --- |
| Rise of the Ember | Cinematic | 1:58 |
| Monsoon Drive | Synthwave | 2:04 |
| Chai & Chill | Lo-fi | 2:04 |
| Neon Bazaar | House | 2:07 |
| Starlit Ghats | Ambient | 2:04 |
| Midnight Circuit | Techno | 2:17 |
| Warehouse 303 | Techno | 2:27 |
| Deep Pulse | Techno | 2:15 |
| Steel Monsoon | Techno | 2:23 |

## Add your own songs

Only add songs you made yourself or have a licence to use, such as royalty-free or Creative Commons music (credit the artist if the licence asks for it).

### Option 1: Add songs button (on your device)

Open Library and tap **Add songs**, then pick MP3, M4A or WAV files. They play in Beatz and stay in that browser on that device; nothing is uploaded. On a computer you can also drag files onto the page.

Name files `Artist - Title.mp3` and Beatz fills in the artist and title for you.

### Option 2: The songs folder (for everyone who opens your site)

1. Put your audio files in the `songs` folder of this repository.
2. List each one in `songs/songs.json`:

```json
{
  "songs": [
    { "file": "my-first-song.mp3", "title": "My First Song", "artist": "Rahul", "genre": "Pop" },
    { "file": "night-walk.mp3", "title": "Night Walk", "artist": "Rahul" }
  ]
}
```

3. Commit and push. The songs appear under **Songs folder** in Library and on Home.

This option needs the app to be served over the web, for example with GitHub Pages (Settings → Pages → branch `main`). It does not work when you open `index.html` straight from your files.

GitHub blocks single files over 100 MB, so keep each song well under that (a 4-minute MP3 is usually 4 to 10 MB).

## Run it

Open `index.html` in a browser, or serve the folder:

```
npx serve .
```

Tap play to start the sound, since browsers only allow audio after you interact with the page.
