
# SecureVault

**SecureVault** ist ein Passwortmanager für **Android** und **Windows**. Er speichert deine Zugangsdaten verschlüsselt in einem Tresor, füllt sie in Apps und Browsern automatisch aus und hilft dir, schwache, doppelt verwendete und geleakte Passwörter zu finden.

Entwickelt mit **.NET MAUI 10** (C#) als Einzelprojekt von [AerosElectron](https://github.com/AerosElectron).

## Funktionen

### Tresor
- Passwörter, Benutzernamen, E-Mail-Adressen, Websites und Notizen übersichtlich verwalten
- Suchen, Filtern, Sortieren und Mehrfachauswahl in der Passwortliste
- Website-Symbole für schnelle Orientierung
- Eingebauter **Passwortgenerator**
- **Einmalcodes (TOTP)** direkt im Eintrag, ohne zusätzliche Authenticator-App
- **Passkeys** speichern und verwenden (Android)

### Sicherheit
- Der Tresor ist mit **AES-256-GCM** verschlüsselt. Der Schlüssel wird mit **PBKDF2** (SHA-256, 100.000 Runden) aus deinem Tresor-Passwort abgeleitet.
- **Zwei-Faktor-Anmeldung (MFA)** und optional **Biometrie** (Fingerabdruck, Gesicht)
- **Automatische Sperre** nach einer einstellbaren Zeit ohne Eingabe (30 Sekunden bis 30 Minuten)
- **Wiederherstellungsschlüssel**, falls du das Tresor-Passwort vergisst
- **Sicherheitscheck:** erkennt schwache und mehrfach verwendete Passwörter und prüft über die Dienst-Schnittstelle von *Have I Been Pwned*, ob ein Passwort in bekannten Datenlecks vorkommt. Dabei verlässt dein Passwort das Gerät nie, übertragen wird nur ein Teil seines Hashes (k-Anonymität).
- Schutz vor Screenshots und Bildschirmaufnahmen (in den Einstellungen schaltbar)

### Komfort
- **Autofill** für Apps und Browser unter Android, inklusive Speichern und Aktualisieren neuer Zugangsdaten
- **Import** aus Google (Chrome), KeePass, Proton Pass, Bitwarden und Microsoft Authenticator; **Export** als KeePass-CSV
- **Abgleich zwischen Geräten** über deinen eigenen Google-Drive-App-Ordner (verschlüsselte Tresordatei)
- **Automatische Backups** im einstellbaren Zeitabstand, auf dem Gerät und optional in Google Drive
- **Handy-Freigabe:** neue Geräte per QR-Code vom Smartphone bestätigen
- **Benachrichtigungen** über die verbleibende Sperrzeit und neue Updates
- **Automatische Updates:** prüft auf neue Versionen in den GitHub-Releases und lädt sie auf Wunsch herunter

## Unterstützte Plattformen

| Plattform | Mindestversion |
|-----------|----------------|
| Android   | 7.0 (API 24)   |
| Windows   | Windows 10 (Version 1809) oder neuer, Windows 11 empfohlen |

## Installation

1. Öffne den Bereich [**Releases**](https://github.com/AerosElectron/SecureVault/releases) dieses Repositories.
2. Lade die aktuelle Version herunter:
   - **Android:** die `.apk`-Datei. Erlaube bei Nachfrage die Installation aus dieser Quelle.
   - **Windows:** das Setup (`.exe`).
3. Starte SecureVault und lege dein Tresor-Passwort sowie die Zwei-Faktor-Anmeldung fest.
4. **Notiere dir den Wiederherstellungsschlüssel** und bewahre ihn getrennt vom Gerät auf.


