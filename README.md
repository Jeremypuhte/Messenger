# Freier Messenger

Ein Messenger ohne Konzern, ohne Konto und ohne eigenen Server. Die App besteht aus einer einzigen Datei (`index.html`) ohne Abhängigkeiten.

## So funktioniert es

- Jede Person hat einen **6-stelligen Code** (wird beim ersten Start erzeugt, lässt sich ändern).
- Codes tauscht ihr untereinander aus und legt sie in der **Kontaktliste** ab.
- Kontakt antippen startet einen Chat. Die andere Person bekommt eine Anfrage und muss sie **annehmen**. Unbekannte Anfragen werden bei Annahme als Kontakt gespeichert.
- Nachrichten gehen **direkt von Gerät zu Gerät** (WebRTC, verschlüsselt). Kontakte und Verlauf liegen nur lokal im Browser.

## Was über Dritte läuft

Nur die kleinen Verbindungsdaten (wer will mit wem sprechen) laufen über einen öffentlichen Vermittler, standardmäßig [ntfy.sh](https://ntfy.sh). Wer das nicht will, betreibt einen eigenen ntfy-Server (Open Source) und trägt ihn unter **Einstellungen** ein. Für Verbindungen durch Router wird standardmäßig ein öffentlicher STUN-Server genutzt. Das Feld in den Einstellungen leeren schaltet ihn ab, dann klappt es nur im selben Netzwerk.

## Grenzen

- Beide Personen müssen gleichzeitig online sein (kein Offline-Versand)
- Nur Gespräche zu zweit
- Wer deinen Code kennt, kann dir eine Anfrage schicken (nicht mehr). Gib ihn nur an Leute, denen du vertraust, oder erzeuge bei Bedarf einen neuen.

## Veröffentlichen mit GitHub Pages

1. Die drei Dateien in ein neues GitHub-Repository hochladen.
2. **Settings → Pages**, Branch `main`, Ordner `/ (root)`.
3. Die App ist danach unter `https://DEIN-NAME.github.io/REPO-NAME/` erreichbar.

Lokal funktioniert es auch: `index.html` im Browser öffnen.

## Lizenz

MIT, siehe `LICENSE`.
