Hi, ich habe diese Mitlify-Dokuemntation, die ich auf GitHub hoste.

Meine Dokuemntation ist derzeit in 2 Teile geteilt, "Dokumentation - Alt" und "... - Neu".

An der neuen Version möchte ich eine moderne und für meinen Bot, Team-Dashboard und BotDashboard eine passende, nutzerpreundliche und professionelle Dokumentation haben.
Dabei ist es mir wichtig, dass der Aufbau grundlegend gleich pro Thema ist (bspw. Module sind alle selbig aufgebaut, Übersichtsseiten fürs Dashboard,TeamDash und Bot auch usw.). Außerdem soll sie auch einen "Dev"-Tab haben, in dem Mustervorlagen drin sind...


Zuerst möchte ich jedcoh, dass du mir meine ganzen Module einmal einstellen tust, dafür bekommst du immmer den passenden Slash-Befhelt als auch dann die notwendigen Infos. Bitte beachte folgendes: Im Dashboard können die Konfugurationen nur ANGEPASST werden und nicht neu aktiviert werden - bitte überall anpassen und nutzen:

Aktivitätschecks:
/aktivitaet_setup admin_role:@everyone buttons:True (Per Button die Aktität bestätigen oder Emojis) menu:True (Separates Menü zum erstellen senden)
/aktivitaet_create channel:#Allgemein ziel:@everyone ueberschrift:Test text:Test stunden:Laufzeit in Stunden. Nur eine Zahl wie 0.5 (30 min.), 1 (1h)...
/aktivitaet_cancel Abbrechen des Checks ohne ausweertung

Anti-Bot System (Honeypot):
/anti-bot-setup (Menü):
- Überwachungs-Kanal auswählen (Zu trackender Kanal)
- Log-Kanal auswählen
- Bestrafung auswählen (Timeout von 10min, Kick, Ban)
- Whitelist-Rolle(n)
unter "Erweitert":
- Admins ignorieren? (Ja = Nutzer mit Administrator-Rechten werden nicht verwaltet, Nein = ebenfalls überwacht)
- Bots ignorieren? (Ja = alle werden ignoriert, Nein = Bots außer Whitelist werden moderiert)
- Verdächtige Accounts ab x Tagen (1,3,7,14,30,60,90 werden besonders beachtet + extra gemeldet(bei verstoßen))

Auto-Menü (kennzeichensystem/Fahrzeugdatenbank für Adminteams (empfohlen)):
/auto-setup (Menü):
- Prefix setzen: Kennzeichenpräfix festlegen, in amtlichen Kennzeichen aus Deutschland wäre dies die Stadtzulassung ** -- -- (** Präfix), (-- -- Zahlen und Buchstaben durch NUtzer wählbar)
- Team Rolle: Darf alle Autos sehen und eigenes eintragen
- Verwaltungsrolle: Team-Rolle + Verwalten (einschl. löschen)
- Spiel und Fahrzeuge: Vordefinierte Fahrzeugtypen aus Spielen oder "Eigene Fahrzeutypen" (dort max. 10 unterschiedliche)
- Kanal setzen: Kanal in den das Menü kommt
- Log-Kanal (optional): Änderungen, Löschen, Korrigieren, Eitragen werden geloggt
- Abschließen

Das Menü an sich hat folgende Buttons:
- Auto eintragen
- Meine Autos
- Alle Autos
- Verwaltung:
-- Nutzer auswählen, dann Fahrzeug, dann Ändern/Löschen des jeweiligen Kennzeichen
- Nicht Teameinträge löschen: Schaut nach allen Einträgen von Nutzern ohne Team-Rolle und löscht nach Bestätiging diese

Case-Menu (Log/Notationssystem für In-Game bestrafungen durch eintragen der Nutezr):
/case-setup (Menü):
- Kanal für Cases: Kanal, in dem das Case-Menü erscheint.
- Rolle für Case-Verwaltung auswählen: Verwaltungsrolle
Nur Mitglieder mit dieser Rolle dürfen das Case-Menü nutzen.
- (Optional) Statistik-Kanal: Kanal für Statistiken und eine allgemeine Übersichten.
- Beweis erforderlich: Legt fest, ob beim Anlegen eines Cases ein Nachweis (z.B. Screenshot/Clip) angehangen werden kann.
- Kanäle automatisch erstellen (Button): Erstellt einen neue Kategorie, wenn Rechte passend, mit allen Kanälen
- Kanal für Bestrafungen-Logs: Kanal für Protokollierung von Bestrafungen und Exporten.
- Kanal für "Ban ausstehen": Hier werden Nachrichten gesendet, wenn ein Nutezr noch ingame ist und durch einen mit Rechten gebannt werden soll
- (Button) Ban ausstehen aktivieren/deaktivieren

Entbannungssystem (In Kombination mit Case-System zum erstellen von Entbannungsanträgen):
/entbannung_setup (Menü):
- Log-Kanal auswählen: Hier erscheinen die Anträge
- Menü Kanal auswählen
/entbannung_fragen (Menü):
- Fragen bearbeiten (Bis zu 3 weitere Fragen zusätzlich zu "Warum sollten wir dich entbannen?" und "Was wirst du ändern?")
- Fragen löschen
/entbannung_postmenu
- Sendet das Entbannungspanel - wenn es nicht automatisch passiert

Geburtstagssystem:
/birthday-setup (Menü):
- Geburtsgaskanal auswählen: Kanal für Geburtstagspanel und Benachrichtigungen auswählen
- Optionale Geburtsgasrolle: Temporäre Rolle für den Tag an Nutzer, die geburtsag haben

/birthday-set → Tag, Monat und optional Geburtstagsbenachrichtigung auswählen.
Danach erscheint die Datenschutzabfrage; erst mit ✅ Annehmen wird der Geburtstag gespeichert.
/birthday-edit → vorhandenen Geburtstag und Benachrichtigung ändern.
/birthday-delete → sämtliche Geburtstagsdaten vollständig löschen.

/birthday-greet-resend: Sendet eine Benachrichtigung des aktuellen Geburtstabes in den GeburtgasKanal

Giveaway-System:
/giveaway-erstellen dauer:1s, 10m, 1h, 12h, 1d, 7d kanal:Zielkanal - sonst aktueller kanal gewinneranzahl:Zahl preis:Der zu gewinnende Preis beschreibung:Beschreibung
/giveaway-beende: Liste mit aktuellen Giveaways, beendet das entsprechende

Haus-System (Häuserliste mit Verwaltungspanel):
/haus_setup (Menü):
- Listenkanal auswählen
- Verwaltungskanal auswählen (Sendet Verwaltungspanel in den Kanal)
- Verwaltungsrolle
- Liste auswählen (Presets oder "Eigene Bild-URL")
- Häuser & Namen (Button): Anzahl der Häuser, Standartnamen pro Haus, optional eigene Namen
- Karte festlegen: Schnelles Ändern der Karten-Bild URL
!Bild-URL-Hinweis
Hinweis: Discord-CDN- und Nachrichten-Bild-URLs können ablaufen oder nicht dauerhaft angezeigt werden. Lade das Bild bitte bei einem Dienst mit permanentem Direktlink hoch und hinterlege diese Bild-URL. Wenn du keinen Direktlink erstellen kannst/willst, dann melde dich auf dem Supportserver und wir erstellen dir einen Link.!

Ingame-Hilfe System (Sendet einen Alarm, wenn ein Admin Hilfe anfordert):
/hilfe_setup (Menü):
- Kanal für Hilfe Anfragen
- Knaal für "Hilfe Anfordern"-Button
- Rollen, die den Button nutzen dürfen
- Team-Rolle die bei jeder Anfrage gepingt wird
- Panel-Text (Button): Anpassend es Hilfe-Anfordern Embet
- Hilfe-Nachricht (Button): Bearbeiten der Nachricht mit 
- Emojis (Button): Stardartreaktionen des Bots auf die Hilfe-Nachricht
- Cooldown (Button): (Kein Cooldown, 2,5,10,15,30,60min)

Personensystem (Nutzerverzeichnis für Adminteams auf Roblox (empfohlen)):
/personen_setup (Menü):
--- Über Buttons ---
- Team-Rolle (Hinzufügen eigener Einträge+Sehen der Einträge)
- Verwaltungsrolle (Darf bearbeiten, sehen und löschen)
- Hauptmenü-Kanal
- Anfragen Kanal
- Anfragen Menü Kanal
- Log-Kanal (Optional): Sendet Logs bei Rechte-Anfragen, neuen, geänderten oder gelöschten Einträgen
- Vordefinierte Rechte (Möglichkeit, verschiedene Rechtegruppen bei den Rechteanfragen anzugeben)
- Anfragensystem AN/AUS

Das Menü an sich hat folgende Buttons:
- Eintragen/Bearbeiten: ... des eigenen Eintrages
- Mein Eintrag
- Alle Einträge
- Person suchen: (sucht im System nach passenden Nutezrn)
- Fehlende Einträge: Schaut, welche Nutezr der Teamrolle nicht eingetragen sind
- Roblox-Spielerinformationen: Per API Abfarge über einen belibigen gültigen Nutezr
- Verwaltung:
-- Nutzer auswäheln, dann Eintrag bearbeiten oder löschen
- Nicht Teameinträge löschen: Löscht nach bestätigung alle Einträge von Nutzern, die nichtmehr auf dem Server sind

--- Neue Module ---

/serverstatus_setup (Übersichtpanle, dass durch manuelle aktualisierung den Serverfüllstand anzeigt) (Menü):
- Öffentliches Panel Kanal auswählen
- Verwaltungskanal auswählen: (In den kommt das Verwaltungspanel)
- Verwaltungsrolle auswählen

Das Verwalten-Panel hat folgende Buttons:
- Server an
- Server aus
- Serverstatus: Quci-Serverfüllstand mit voll, leer, halbvoll siewie eigene Spieleranzahl
- RP-Sync: Synchonisiert den RP-Status mit dem Panle (sofern Roleplay Management aktiviert ist)
- Informationen: Angabe des Servernamen, Owners und Servercodes
- Spieldaten: Angabe von aktueller, maximaler Spieleranzahl und of gwisse Modi eingeschlatet sind (RP-Modus, Baumodus, VC-Pflicht)
- Rollen: Auswahl der Rollen, die verwalten dürfen
- Öffentliches Panel: Aktualisieren
- Panel aktualisieren: Das Verwaltungspanel

Schichtsystem:
/shift_setup (Menü):
- Team-Rolle: Member, die Schicht starten dürfen
- Verwaltungsrolle: Member, die Schichten für andere beenden und starten können sowie statistiken zu denen sehen
- Satistiken anzeigen Rolle: Darf eigene Schichten starten/stoppen + alle Statistiken einsehen
- On-Duty Rolle: Rolle, die während der Schicht dem Nutzer gegeben wird
- Log-Kanal: Schicht-start/stopp Logs
- Info-Kanal: Benachrichtigungen bei zu langer Schicht und/oder Inaktivität
- Panel-Kanal: Live-Panel mit aktuellen Schicht-Mitgliedern
- Inaktivitätsprüfung umschalten: AN/AUS
-> Im Dashboard sind gewisse Richtlinien zu Zeiten anpassbar

Teamliste (Pro-Feature):
/teamliste_setup (Menü):
- Startet Setup-Wizzard für bis zu 25 Rollen
-> Rolle aus Dropdown auswählen, ggf. Name bearbeiten
- "höchste Rolle" bedeutet, dass wenn an nur die höchste Rolle des Nutzers auch den Nutzer in der Liste zeigt, ansonsten alle Rollen der Teamliste, die der Nutezr auch hat

Ticket-System (Pro-Feature):
/ticket-setup (Menü):
- Setup öffnen, Anpassen des Panel Titel, der Willkommensnachricht im Ticket, Anzahl der unterschiedlichen Ticket-Arten (max. 4) sowie Bezeiuchnungen dieser sowie optionale Bild-Banner URL