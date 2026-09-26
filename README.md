# Marcus Modus DBT Podcast — RSS Feed

Selbst gehosteter RSS-Feed fuer die Podcast-Distribution (Spotify for Creators, Apple Podcasts
u. a.) der Marcus-Modus-DBT-Videos. Wird ausschliesslich vom Automations-Skript
`F:/MarcusModus/videoCreation/videoCreationWorkflow/13 SpotifyPodcast/toolUse/rss_feed_update.py` in Schritt 13 des Video-Creation-Workflows
geschrieben — siehe dortiges `How-to Spotify-Podcast-RSS-Setup.md` fuer den vollstaendigen
Prozess. Nicht von Hand editieren, ausser fuer einmalige Notfall-Korrekturen.

- **Feed-URL:** https://thejosegu.github.io/marcus-modus-podcast-feed/rss.xml
- **Hosting:** GitHub Pages (main-Branch, Root)
- **Audio:** `episodes/*.mp3`, je eine Folge = die fertig gemischte Tonspur eines Marcus-Videos
- **Show-Cover:** `cover/2026-09-v3/show-dbt-im-alltag.jpg`, 3000x3000 RGB,
  mit "MARCUS MODUS / DBT IM ALLTAG". Bestehendes Marcus-Motiv weiterverwendet.
- **Folgenbilder:** jede Folge hat ein eigenes `itunes:image` mit Nummer und maximal
  zwei Themenwoertern und der grossen Dachzeile "DBT IM ALLTAG".
  Bestand unter `cover/2026-09-v3/`, neue Folgen unter `cover/episodes/`.
  Die Nummer steht auch im RSS-Feld `itunes:episode`.
- **Nummerierung:** 01–26 bleiben erhalten; 27 ist fuer Gedankenkarussell reserviert
  (noch nicht im Feed), Neid ist 28. Keine bestehende Folge umnummerieren.
- **YouTube:** Beschreibungen enthalten den Link zur oeffentlichen Langfassung.
  Stand 26.09.2026: 25 Links; Schuldgefuehle und Scham sind auf YouTube privat und
  bekommen erst nach einer gesonderten Freigabe einen Link. Videos nicht automatisch freigeben.

Die Cover-Umstellung vom 26.09.2026 aendert weder Audiodateien noch GUIDs,
Audio-URLs oder Veroeffentlichungsdaten. Eingebettete MP3-Bilder bleiben unveraendert;
Podcast-Verzeichnisse erhalten die neuen Bilder ueber RSS. OP3 ist noch nicht aktiviert.

## Einmalige Einrichtung bei Spotify

1. In [Spotify for Creators](https://creators.spotify.com) eine neue Show anlegen ueber
   "Bestehende Show suchen" -> "Woanders" -> obige Feed-URL eintragen.
   *(Erneuter Anlauf: "Ich moechte einen neuen Podcast starten" -> "Feed importieren", je nach
   aktueller UI-Beschriftung.)*
2. Spotify sendet einen Verifizierungscode an die in `itunes:owner/itunes:email` hinterlegte
   Adresse (`j.sebastian.guenther@gmail.com`).
3. Danach holt Spotify neue `<item>`-Eintraege automatisch, sobald sie im Feed erscheinen --
   kein erneuter manueller Schritt pro Folge noetig.

Cover-Farben: DBT IM ALLTAG hellblau (#8BD2F9), Folgentitel und Nummer weiss.
