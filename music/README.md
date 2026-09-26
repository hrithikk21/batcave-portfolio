# Music folder

Drop a background track in here and the site's Music control will pick it
up automatically — no code changes needed.

## Expected file names

```
music/
├── theme.ogg   ← preferred (smaller, open format)
├── theme.mp3   ← fallback for browsers that don't support OGG
└── README.md   ← this file
```

You only need **one** of the two files. If you add both, browsers that
support OGG will use it first and fall back to MP3 automatically.

## Where to get a track

Do not use copyrighted commercial music without a license. Good sources
for a royalty-free / properly licensed ambient or cinematic track:

- Your own recording or an original composition
- A track explicitly marked royalty-free / CC0 from a library such as
  Pixabay Music, Free Music Archive, or a purchased license from a site
  like Epidemic Sound or Artlist

Something dark, ambient and low-key (think "quiet cave hum", not a full
band) fits the site's tone best. Keep the file reasonably small
(under ~4–5 MB) so the portfolio stays fast to load — the audio only
loads when the visitor actually presses play (`preload="none"`).

## If no file is present

That's fine — the site is fully functional without one. The Music
control will show a friendly "no track found" message instead of
breaking, and every other feature (sound effects, the generated ambient
score, the terminal, etc.) keeps working normally.
