# SatFeeds

**Deutsch** | [English](#english)

SatFeeds ist ein Plugin für Enigma2 (getestet mit OpenATV 8.0.1 auf einem Octagon SF8008). Es zeigt die aktuellen Live-Feed-Meldungen von [www.satelliweb.com](https://www.satelliweb.com) an und stellt die Feeds der letzten Stunden als eigenes Bouquet mit EPG-Text bereit.

## Funktionen

- Hauptfenster mit Tabelle aller gespeicherten Feeds (Zeit, Feed-Art, Sat-Position, Frequenz, SR, Beschreibung); OK schaltet auf den Feed um
- Bouquet mit EPG-Text, gegliedert nach Format (4:2:0 / 4:2:2 / verschlüsselt) oder nach Kategorie
- Filter nach Satellitenpositionen und Feed-Arten
- Abrufintervall 3, 5 oder 10 Minuten oder aus, mit bedingter Abfrage (kleine Antwort, wenn sich die Seite nicht geändert hat)
- Zweite Feedquelle (optional): Feedmeldungen aus dem Forum rolisat.de, einzeln oder zusammen mit Satelliweb; Spalte „Quelle“ in der Liste
- Zap-Meldung beim Umschalten auf einen Feed
- Monatsstatistik mit Vormonatsvergleich
- Deutsch und Englisch, je nach Spracheinstellung der Box
- Update-Prüfung (Standard: aus), Installation nur nach Bestätigung

## Download und Installation

Aktuelle Version: **3.0**

- [Plugin (.ipk)](https://github.com/feedhunter/satfeeds/releases/download/v3.0/enigma2-plugin-extensions-satfeeds_3.0_all.ipk)
- [Anleitung (PDF, Deutsch)](https://github.com/feedhunter/satfeeds/releases/download/v3.0/SatFeeds_Anleitung_DE.pdf)
- [Manual (PDF, English)](https://github.com/feedhunter/satfeeds/releases/download/v3.0/SatFeeds_Manual_EN.pdf)
- [Changelog (Deutsch)](https://github.com/feedhunter/satfeeds/releases/download/v3.0/CHANGELOG_Satfeeds_de.txt) · [Changelog (English)](https://github.com/feedhunter/satfeeds/releases/download/v3.0/CHANGELOG_Satfeeds_en.txt)
- [Alle Versionen](https://github.com/feedhunter/satfeeds/releases)

Die Datei `.ipk` nach `/tmp` auf die Box kopieren und im Terminal ausführen:

```
opkg install --force-reinstall /tmp/enigma2-plugin-extensions-satfeeds_3.0_all.ipk
```

Danach fragt die Box, ob die GUI neu gestartet werden soll. Alternativ: `killall -9 enigma2`.

## Update-Prüfung

Ist die Einstellung „Update-Prüfung“ eingeschaltet (Standard: aus), fragt das Plugin einmal täglich die Datei `version.json` in diesem Repository ab und zeigt im Hauptfenster einen Hinweis, wenn eine neuere Version vorliegt. Von Hand geht es über MENU → „Nach Update suchen“. Es wird nichts ohne Bestätigung installiert. Vor der Installation prüft das Plugin Größe und SHA-256-Prüfsumme der Datei. Bei der Abfrage übertragen wird nur die übliche Verbindungsinformation (IP-Adresse der Box), keine weiteren Daten.

## Datenquelle und Bedingungen

Die Feed-Daten stammen von [www.satelliweb.com](https://www.satelliweb.com) und – optional, über die Einstellung „Quelle der Feeds“ – aus dem Feedmeldungen-Forum von [rolisat.de](http://rolisat.de/phpBB/index.php). Die Betreiber haben das Auslesen unter diesen Bedingungen erlaubt (Satelliweb auch die Weitergabe des Plugins):

- kostenlos und nicht kommerziell
- keine zusätzlichen Anfragen an die Seite
- Quellenangabe mit Link auf www.satelliweb.com (im Hauptfenster des Plugins)

Bitte beachtet diese Bedingungen und stellt das Abrufintervall nicht kürzer als vorgesehen ein. Für die Nutzung der Daten gelten die Nutzungsbedingungen von Satelliweb.

## Hinweise

- Die Feeds sind Livemeldungen von Nutzern. Ob ein Feed bei euch empfangbar ist, hängt vom Empfang ab (Schüssel, Rotor, Position).
- Getestet nur auf einem Octagon SF8008 mit OpenATV 8.0.1 und den Skins MetrixHD und HDglass17. Auf anderen Boxen, Images oder Skins kann die Darstellung abweichen.
- Das Plugin wird ohne Gewähr bereitgestellt. Es ist ein privates Hobbyprojekt und steht in keiner Verbindung zu Satelliweb oder Rolisat.

Autor: feedhunter

---

## English

SatFeeds is a plugin for Enigma2 (tested with OpenATV 8.0.1 on an Octagon SF8008). It shows the current live feed reports from [www.satelliweb.com](https://www.satelliweb.com) and provides the feeds of the last hours as a bouquet of its own, with EPG text.

### Features

- Main window with a table of all stored feeds (time, feed type, sat position, frequency, SR, description); OK zaps to the feed
- Bouquet with EPG text, grouped by format (4:2:0 / 4:2:2 / encrypted) or by category
- Filters for satellite positions and feed types
- Fetch interval of 3, 5 or 10 minutes, or off, with conditional requests (small response if the page has not changed)
- Second feed source (optional): feed reports from the forum rolisat.de, alone or together with Satelliweb; column "Source" in the list
- Message when zapping to a feed
- Monthly statistics with comparison to the previous month
- Save feeds (key 0) and show them (key PLAY, with category, filter by category and text search; delete entries again): your own archive to see when a feed was on air before, on which satellite and with which parameters (data or parts of the parameters often repeat)
- German and English, depending on the language setting of the receiver
- Update check (default: off), installs only after your confirmation

### Download and installation

Current version: **3.0**

- [Plugin (.ipk)](https://github.com/feedhunter/satfeeds/releases/download/v3.0/enigma2-plugin-extensions-satfeeds_3.0_all.ipk)
- [Manual (PDF, English)](https://github.com/feedhunter/satfeeds/releases/download/v3.0/SatFeeds_Manual_EN.pdf) · [Anleitung (PDF, Deutsch)](https://github.com/feedhunter/satfeeds/releases/download/v3.0/SatFeeds_Anleitung_DE.pdf)
- [Changelog (English)](https://github.com/feedhunter/satfeeds/releases/download/v3.0/CHANGELOG_Satfeeds_en.txt) · [Changelog (Deutsch)](https://github.com/feedhunter/satfeeds/releases/download/v3.0/CHANGELOG_Satfeeds_de.txt)
- [All versions](https://github.com/feedhunter/satfeeds/releases)

Copy the `.ipk` file to `/tmp` on the receiver and run in a terminal:

```
opkg install --force-reinstall /tmp/enigma2-plugin-extensions-satfeeds_3.0_all.ipk
```

The receiver then asks whether to restart the GUI. Alternatively: `killall -9 enigma2`.

### Update check

If the setting "Update check" is switched on (default: off), the plugin reads the file `version.json` in this repository once a day and shows a note in the main window when a newer version is available. You can also check by hand via MENU → "Check for updates". Nothing is installed without your confirmation. Before installing, the plugin checks size and SHA-256 checksum of the file. The request transmits only the usual connection information (the receiver's IP address), no other data.

### Data source and conditions

The feed data comes from [www.satelliweb.com](https://www.satelliweb.com) and – optionally, via the setting "Source of the feeds" – from the feed-reports forum of [rolisat.de](http://rolisat.de/phpBB/index.php). The operators have permitted reading the data under these conditions (Satelliweb also the sharing of the plugin):

- free of charge and non-commercial
- no additional requests to the site
- credit with a link to www.satelliweb.com (shown in the plugin's main window)

Please respect these conditions and do not set the fetch interval shorter than provided. The terms of use of Satelliweb apply to the use of the data.

### Notes

- The feeds are live reports from users. Whether a feed can be received at your location depends on your setup (dish, rotor, position).
- Tested only on an Octagon SF8008 with OpenATV 8.0.1 and the skins MetrixHD and HDglass17. The display may differ on other receivers, images or skins.
- The plugin is provided without warranty. It is a private hobby project and not affiliated with Satelliweb or Rolisat.

Author: feedhunter
