# 🎉 Partykiste

**Partyspiele für ein Handy – einfach weitergeben.**

Partykiste ist eine Web-App mit zehn Partyspielen für Spieleabende mit Freunden. Ihr braucht nur ein einziges Handy, das reihum geht. Die App funktioniert offline, merkt sich alle Einstellungen und ist für das iPhone optimiert.

---

## 🎮 Die Spiele

| Spiel | Spieler | Worum es geht |
|---|---|---|
| 🕵️ **Spion** | 3–20 | Alle kennen das geheime Wort – bis auf den Spion. Mit Undercover-Modus, Chaos-Modus, eigenen Wortlisten und geheimer Abstimmung mit Punkten. |
| 🐺 **Werwolf** | 5–20 | Die App führt mit Erzählerstimme durch die Nacht. 8 Sonderrollen: Seherin, Hexe, Jäger, Amor, Beschützer, Ältester, Dorfdepp, Kleines Mädchen. |
| 🤔 **Wer würde eher?** | ab 3 | Auf drei zeigen alle auf eine Person. Am Ende gibt es Titel für jeden. |
| 🎭 **Wer bin ich?** | 2–12 | Ja/Nein-Fragen stellen, bis man errät, wer oder was man ist. Weniger Fragen = mehr Punkte. |
| 📱 **Stirnraten** | 2–12 | Handy an die Stirn, die anderen erklären. Nach unten kippen = richtig, nach oben = weiter. |
| 🎯 **Schätzen** | 2–12 | Knifflige Fragen mit Zahlen als Antwort. Eingabe per Drehrad oder Tastatur, faire oder absolute Wertung. |
| 💣 **Wortbombe** | 2–16 | Wort zur Kategorie sagen und schnell weitergeben – bevor die Bombe hochgeht. |
| 🚫 **Tabu** | 2–4 Teams | Begriffe erklären, ohne die fünf verbotenen Wörter zu benutzen. |
| 🤥 **Zwei Wahrheiten, eine Lüge** | 3–12 | Drei Aussagen über sich erzählen – eine davon ist gelogen. |
| 🙋 **Ich hab noch nie …** | ab 2 | Hand hoch, wer es schon getan hat. Mit optionalem Finger-Zählen. |

---

## ✨ Funktionen

- **Geheime Karten:** Rollen und Wörter liegen unter einer Abdeckung, die man mit dem Finger hochschiebt. Lässt man los, gleitet sie zurück. Bereits angesehene Karten werden deutlich markiert.
- **Erzählerstimmen:** Vier aufgenommene Stimmen (Helmut, Mila, Leonard, Tessa) oder die Computerstimme des Geräts.
- **Ruhiges Design:** Dunkles Farbschema mit eigener Farbe pro Spiel, Glas-Optik im iOS-Stil und sanften Animationen. Bei „Bewegung reduzieren“ werden Animationen automatisch abgeschaltet.
- **Suche und Favoriten** auf der Startseite.
- **Einstellungen** (Zahnrad unter der Suche): Erzählerstimme, Soundeffekte, Ansagen, Konfetti, weniger Bewegung, Daten zurücksetzen und nach Updates suchen.
- **Offline-fähig:** Nach dem ersten Öffnen läuft alles ohne Internet.
- **Datensparsam:** Keine Anmeldung, kein Tracking. Alles wird nur lokal auf dem Gerät gespeichert.
- **Bildschirm bleibt an** während eines Spiels.
- **Schutz vor versehentlichem Verlassen:** Ein laufendes Spiel fragt vor dem Beenden nach.

---

## 📲 Installation auf dem iPhone

1. Die GitHub-Pages-Adresse dieses Projekts in **Safari** öffnen.
2. Auf **Teilen** tippen und **„Zum Home-Bildschirm“** wählen.
3. Partykiste vom Home-Bildschirm starten – sie läuft dann wie eine eigene App im Vollbild.

> Tipp: Werwolf einmal mit Internet öffnen, damit die Erzählerstimmen für den Offline-Betrieb gespeichert werden.

---

## 📁 Aufbau

```
partykiste/
├── index.html              Die komplette App (HTML, CSS, JavaScript)
├── sw.js                   Service Worker für den Offline-Betrieb
├── manifest.webmanifest    App-Name, Farben und Icons
├── icon.svg                App-Icon (Vektor)
├── icon-192.png            App-Icon
├── icon-512.png            App-Icon
├── apple-touch-icon.png    Icon für den iPhone-Home-Bildschirm
└── audio/
    ├── SPRECHTEXTE.md      Alle Sprechtexte mit Dateinamen
    ├── helmut/             36 Aufnahmen (männlich)
    ├── mila/               36 Aufnahmen (weiblich)
    ├── leonard/            36 Aufnahmen (männlich)
    └── tessa/              36 Aufnahmen (weiblich)
```

Die App kommt ohne Frameworks und ohne Build-Schritt aus. Einfach alle Dateien hochladen – fertig.

---

## 🎙️ Eigene Stimmen hinzufügen

Die Erzählerstimmen wurden mit ElevenLabs erzeugt. Eine weitere Stimme lässt sich so ergänzen:

1. Alle Texte aus `audio/SPRECHTEXTE.md` einsprechen lassen.
2. Die Dateien als MP3 genau nach der Tabelle benennen (z. B. `ww_night1.mp3`).
3. In einen neuen Ordner unter `audio/` legen, z. B. `audio/neuername/`.
4. In der `index.html` die Liste `VOICES` um die neue Stimme ergänzen.

Fehlende Dateien ersetzt Werwolf automatisch durch die Computerstimme.

---

## 🔄 Updates

Nach jeder Änderung die Versionsnummer in `sw.js` erhöhen (z. B. `partykiste-v19` → `partykiste-v20`). Öffnet man die App danach mit Internet, lädt sie die neue Version im Hintergrund und zeigt unten „✨ Neue Version ist bereit – Neu laden“. Ohne neue Versionsnummer bleibt die alte, gespeicherte Version aktiv.

---

<p align="center">Mit ♥ gemacht von Kerem</p>
