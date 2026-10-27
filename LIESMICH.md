# Fotowerk – Galerie ausmisten (Android)

Swipe-App für die Handy-Galerie: **links = zum Löschen vormerken, rechts = behalten**.
Fotowerk sortiert vor (unscharf, zu dunkel, überbelichtet, Serien/ähnliche Fotos) und verschiebt
vorgemerkte Fotos gesammelt in den **Papierkorb** (30 Tage wiederherstellbar). Alles bleibt auf dem Handy.

Voraussetzung: Android 11 oder neuer.

## App bauen (einmalig, kostenlos über GitHub)
1. Bei github.com ein Konto anlegen und anmelden.
2. Oben rechts **+ → New repository**, Name `fotowerk`, **Private**, **Create repository**.
3. Auf der neuen Seite auf **„uploading an existing file“** klicken.
4. Den **Inhalt** des entpackten Ordners `fotowerk` (alle Dateien und Ordner, auch `.github`) ins Fenster ziehen.
   Wird `.github` nicht angezeigt: im Windows-Explorer unter „Ansicht“ die ausgeblendeten Elemente einblenden.
5. Unten **Commit changes** klicken.
6. Oben auf **Actions**: Der Bau „Fotowerk bauen“ läuft (ca. 5 Minuten, grüner Haken = fertig).
7. Auf der Startseite des Repositorys rechts unter **Releases** → neueste Version → **Fotowerk.apk**.

## Auf dem Handy installieren
1. Am Handy bei github.com anmelden, Release öffnen und **Fotowerk.apk** herunterladen.
2. Datei antippen. Android fragt einmal, ob der Browser Apps installieren darf → **Erlauben**.
3. Fotowerk öffnen und beim Fotozugriff **„Alle zulassen“** wählen.

## Benutzen
- **Vorsortierte prüfen:** nur verdächtige Fotos (unscharf, zu dunkel/hell, schlechtere Fotos einer Serie).
- **Alle Fotos durchgehen:** alles, was du noch nicht angeschaut hast.
- Wischen oder Knöpfe: ✕ Löschen / ↶ Rückgängig / Behalten ✓.
- **Zum Löschen vorgemerkt ansehen:** nochmal prüfen; antippen = doch behalten.
- **In den Papierkorb:** Android fragt einmal zur Bestätigung.
- Behaltene Fotos werden nicht mehr angezeigt (zurücksetzen über den Knopf unten auf der Startseite).

## Anpassen (optional)
In `app/src/main/java/de/fotowerk/app/MainActivity.kt` oben:
`BLUR_LIMIT` (Unschärfe, höher = strenger), `DARK_LIMIT`, `BRIGHT_LIMIT`,
`SERIES_MS` (Serien-Abstand in ms), `SERIES_HAMMING` (Ähnlichkeit, höher = großzügiger).
Nach einer Änderung baut GitHub automatisch eine neue Version; sie installiert sich als Update über die alte.
