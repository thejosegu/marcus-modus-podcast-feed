# Marcus Modus DBT Podcast — RSS Feed

Selbst gehosteter RSS-Feed fuer die Podcast-Distribution (Spotify for Creators, Apple Podcasts
u. a.) der Marcus-Modus-DBT-Videos. Wird ausschliesslich vom Automations-Skript
`13 SpotifyPodcast/toolUse/rss_feed_update.py` im Vault `F:\Video\_videoCreationWorkflow`
geschrieben — siehe dortiges `How-to Spotify-Podcast-RSS-Setup.md` fuer den vollstaendigen
Prozess. Nicht von Hand editieren, ausser fuer einmalige Notfall-Korrekturen.

- **Feed-URL:** https://thejosegu.github.io/marcus-modus-podcast-feed/rss.xml
- **Hosting:** GitHub Pages (main-Branch, Root)
- **Audio:** `episodes/*.mp3`, je eine Folge = die fertig gemischte Tonspur eines Marcus-Videos
- **Cover:** `cover/cover-941.png` -- **Platzhalter, nur 941x941px.** Spotify empfiehlt
  mindestens 1400x1400, ideal 3000x3000. Vor der ersten echten Einreichung bei Spotify durch
  ein hochaufgeloestes Cover ersetzen.

## Einmalige Einrichtung bei Spotify

1. In [Spotify for Creators](https://creators.spotify.com) eine neue Show anlegen ueber
   "Bestehende Show suchen" -> "Woanders" -> obige Feed-URL eintragen.
   *(Erneuter Anlauf: "Ich moechte einen neuen Podcast starten" -> "Feed importieren", je nach
   aktueller UI-Beschriftung.)*
2. Spotify sendet einen Verifizierungscode an die in `itunes:owner/itunes:email` hinterlegte
   Adresse (`j.sebastian.guenther@gmail.com`).
3. Danach holt Spotify neue `<item>`-Eintraege automatisch, sobald sie im Feed erscheinen --
   kein erneuter manueller Schritt pro Folge noetig.
