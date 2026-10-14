# Beatzyr

A Spotify-style music player prototype that runs entirely in the browser as a single `index.html` file.

Every song is composed live with the Web Audio API, so there are no audio files and nothing to license.

## Features

- Home, Search, Library and Queue pages
- Curated playlists, artist and genre pages, and Liked Songs
- Your own playlists: create, add songs, remove songs, delete
- Play/pause, next/previous, seek, shuffle, repeat (all or one), volume
- Full-screen Now Playing view with a live audio visualizer, tempo and key
- On phones, a bottom tab bar with a colour for each section: Home, Search, Library and Queue

Likes and playlists are saved in your browser's local storage.

## Run it

Open `index.html` in a browser, or serve the folder:

```
npx serve .
```

Tap play to start the sound, since browsers only allow audio after you interact with the page.
