# Brainclash

Quiz-Duelle mit Freunden im Browser: 10-Runden-Duelle, Einzelspieler-Rangspiel, Themen-Quiz, 1×1-Trainer, Aufstieg, Online-Lobby mit Chat und Einladungslinks.

## Dateien

| Datei | Zweck |
|---|---|
| `index.html` | Das komplette Spiel (eine Datei) |
| `firestore.rules` | Sicherheitsregeln für die Firebase-Datenbank |

## Einrichtung in Kurzform

1. Firebase-Projekt anlegen, **Anonyme Anmeldung** aktivieren, **Firestore** anlegen.
2. Inhalt von `firestore.rules` in Firestore → Regeln einfügen und veröffentlichen.
3. Web-App im Firebase-Projekt registrieren und die angezeigten Konfigurationswerte oben in `index.html` bei `FIREBASE_CONFIG_RAW` eintragen.
4. `index.html` in ein öffentliches GitHub-Repository hochladen und unter Settings → Pages veröffentlichen (Deploy from a branch → `main` → `/ (root)`).
5. Link öffnen, Namen eingeben, über „Freunde per Link einladen“ teilen.

## Hinweise

- Die Firebase-Konfiguration (apiKey usw.) ist für Web-Apps öffentlich gedacht. Geschützt werden die Daten durch `firestore.rules`.
- Jeder Spieler wird anonym über sein Gerät/seinen Browser erkannt. Wer Browserdaten löscht oder das Gerät wechselt, startet mit einem neuen Profil.
- Kostenloser Firebase-Tarif (Spark): 50.000 Lesezugriffe und 20.000 Schreibzugriffe pro Tag – für eine Freundesgruppe mehr als genug.
