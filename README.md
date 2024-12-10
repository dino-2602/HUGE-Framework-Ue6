# Huge Framework - Benutzerregistrierung mit Administrator-Funktion

## Übersicht
Dieses Projekt ist eine angepasste Implementierung des Huge Frameworks, die es ermöglicht:
- Benutzer ohne Captcha zu registrieren.
- Benutzer ohne E-Mail-Verifikation direkt zu aktivieren.
- Administratoren die Möglichkeit zu geben, Benutzer über dasselbe Formular anzulegen.

## Features
- **Nur Administratoren können Benutzer anlegen:** Die `Register`-Seite ist nur sichtbar, wenn ein Administrator eingeloggt ist.
- **Captcha deaktiviert:** Benutzer können sich ohne Captcha registrieren.
- **Direkte Benutzeraktivierung:** Neue Benutzer werden direkt aktiv und müssen ihre E-Mail nicht bestätigen.

## Technologien
![PHP](https://img.shields.io/badge/PHP-7.4%2B-blue?logo=php&logoColor=white)
![Huge Framework](https://img.shields.io/badge/Huge_Framework-1.0-brightgreen)
![HTML](https://img.shields.io/badge/HTML-5-orange?logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-3-blue?logo=css3&logoColor=white)
![PHPStorm](https://img.shields.io/badge/IDE-PHPStorm-purple?logo=phpstorm&logoColor=white)
![MySQL](https://img.shields.io/badge/Database-MySQL-lightblue?logo=mysql&logoColor=white)

## Schritte zur Umsetzung

1. **Captcha deaktiviert:**
   - Entfernt die Captcha-Validierung aus der Registrierung.

2. **E-Mail-Verifikation entfernt:**
   - Benutzer werden bei der Registrierung direkt aktiviert (`user_active = 1`).
   - Entfernt den Aktivierungs-Hash und die Logik zur Verifikations-E-Mail.

3. **Admin-Check für Registrierung:**
   - Nur Benutzer mit einer Admin-Rolle (`account_type: admin`) können neue Benutzer registrieren.
   - Implementiert durch eine Prüfung in der `RegisterController.php`.

4. **Layout-Optimierung:**
   - Die `Register`-Seite wird nur angezeigt, wenn ein Admin eingeloggt ist.

## Screenshots
Screenshots sind in der Dokumentation enthalten, um die Funktionalität zu demonstrieren.

 **Login-Seite(User-Ansicht)**
 
![Benutzerregistrierung](https://github.com/dino-2602/HUGE-Framework-Ue6/blob/main/huge/screenshots/user_regi.png)

 **Account verifiziert(User-Ansicht)**

![Account-ohne-verifizierung-erstellt](https://github.com/dino-2602/HUGE-Framework-Ue6/blob/main/huge/screenshots/user_crea.png)

 **Login-Seite(Admin-Ansicht)**

 ![Anmeldung-Admin](https://github.com/dino-2602/HUGE-Framework-Ue6/blob/main/huge/screenshots/only_admin_login.png)

 **Admin-Account(Mit-Register-Button)**

 ![Registrierung-nur-als-Admin-möglich](https://github.com/dino-2602/HUGE-Framework-Ue6/blob/main/huge/screenshots/admin_login.png)

## Installation
1. Klone dieses Repository:
   ```bash
   git clone https://github.com/dein-benutzername/huge-framework-registration.git
