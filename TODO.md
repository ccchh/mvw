# Projektanforderungen

* Webbasiert
* Python
* Framework: Django oder Flask
* Object Relational Mapper
* Datenbank: SQLite

### Ausbaustufe 1
* Login/Logout
* Verwaltung von Stammdaten
* Eintragen neuer Mitglieder
* Mitgliedersuche (Fuzzy)
* Web-UI sollte mit der Tastatur zu bedienen sein
* Erfa-Statistik
* Zahlungen von Hand einpflegen
* Chaosnummer nicht doppelt vergeben!

### Ausbaustufe 2
* Elektronisches Anmeldeformular
  * Getrennter Service
  * Lagerung der Daten?
* Mahnläufe

### Ausbaustufe 3
* Config im Backend ändern
* Änderung von Mitgliedsbeitrag
* Terminliche Austragung mit Reminder-Mail
* Office-Email Bearbeitung (RT-Like)
* Automatisierte Mahnläufe


# Objektmodell

### User
* Username
* Password
* E-Mail
* isActive

### Stammdaten
* Chaosnummer (PK)
* Organisation
* Vorname
* Nachname
* Anschrift
* Anschrift2
* Land
* PLZ
* Ort
* Adresse Unbekannt/Verzogen
* E-Mail
* Email gültig
* PGP-KeyId
* Extern verwaltet
* IBAN
* BIC
* Kontoeinzug

### Mitglied
* Chaosnummer (FK)
* Datum Eingetreten
* Mitgliedsstatus (Vollzahler/Ehrenmitglied/Ermäßigt)
* Datum Ausgetreten
* Konto-Guthaben
* Keine Datenschleuder
* ...

### DS-Mitglied
* Chaosnummer (PK)
* Abonniert bis
* Konto Guthaben
* ...