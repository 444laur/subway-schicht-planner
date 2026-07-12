# Lastenheft – Digitales Personaleinsatzplanungssystem (PEP)
**Projekt:** Subway Filiale [Name/Standort]  
**Dokumenten-ID:** LH-PEP-2026-001  
**Version:** 1.0  
**Datum:** 2026-07-12  
**Status:** Freigegeben zur Angebotserstellung  
**Verantwortlicher Auftraggeber:** Filialleiter  

---

## 1. Projektgrundlage & Zielsetzung

Die Filiale betreibt ein hohes Besucheraufkommen an einem zentralen Standort. Der wöchentliche Schichtplan wird derzeit manuell und ohne digitale Assistenzsysteme erstellt. 

**Primäres Projektziel:** Die Einführung einer webbasierten oder app-gestützten Planungssoftware, die automatisierte Kollisionsprüfungen ermöglicht, die Einhaltung arbeitsrechtlicher Vorgaben sicherstellt und den Kommunikationsprozess (Planverteilung) standardisiert und entlastet.

---

## 2. Ausgangssituation (Ist-Zustand)

### 2.1 Personalstruktur
Die Filiale verfügt über **10 Mitarbeitende** in folgender Aufteilung:

| Kategorie | Anzahl | Vertragsart | Besonderheit |
| :--- | :--- | :--- | :--- |
| **Vollzeitkräfte (FT)** | 5 | 39 Std./Woche | Feste Grundverfügbarkeit, kein Nebeneinkommen (primäre Einsatzreserve). |
| **Teilzeitkräfte (PT)** | 4 | 15–25 Std./Woche | **Haben weitere feste Arbeitsverhältnisse** (zweiter Job, Studium mit Werksstudierendenvertrag). |
| **Minijobber (MJ)** | 1 | 520€-Basis | **Hat weitere feste Arbeitsverhältnisse** (Geringfügige Nebenbeschäftigung). |
| **Minderjährige** | 0 | - | *Keine Anwendung des JArbSchG erforderlich.* |

### 2.2 Betriebliche Öffnungszeiten
Die Ladenöffnungszeiten variieren nach Wochentag. Der Service endet mit dem Schließen der Tür; die Nachbereitung (Reinigung, Kassensturz) erfolgt in den darauffolgenden 30 Minuten mit vollem Team.

| Wochentag | Öffnungszeit | Ladenschluss (Ende Service) | Voraussichtliche Reinigungszeit |
| :--- | :--- | :--- | :--- |
| Sonntag | 10:00 Uhr | 20:30 Uhr | 20:30 – 21:00 Uhr |
| Montag | 10:00 Uhr | 20:30 Uhr | 20:30 – 21:00 Uhr |
| Dienstag | 10:00 Uhr | 20:30 Uhr | 20:30 – 21:00 Uhr |
| Mittwoch | 10:00 Uhr | 20:30 Uhr | 20:30 – 21:00 Uhr |
| Donnerstag | 10:00 Uhr | 22:00 Uhr | 22:00 – 22:30 Uhr |
| Freitag | 10:00 Uhr | 22:00 Uhr | 22:00 – 22:30 Uhr |
| Samstag | 10:00 Uhr | 22:00 Uhr | 22:00 – 22:30 Uhr |

---

## 3. Definierte Hard Facts & Rahmenbedingungen (Soll-Vorgaben)

Folgende betriebliche und gesetzliche Regeln sind **nicht verhandelbar** und müssen vom System automatisch geprüft und bei Verstößen alarmiert werden:

1.  **Mindestbesetzung zu Rush-Hours:** 
    - Zwischen **12:00–14:00 Uhr** und **17:00–19:00 Uhr** müssen zwingend **4 Mitarbeitende** gleichzeitig im Servicebereich (Theke, Kasse, Backofen/Prep) eingesetzt sein. Unterschreitungen führen zu Umsatzverlusten und sind systemseitig zu unterbinden.
2.  **Closing-Shift (Ladenschluss):** 
    - Ab 30 Minuten vor Ladenschluss bis zum Verlassen des Ladens müssen **mindestens 2 Mitarbeitende** anwesend sein (Sicherheitsvorschrift der Berufsgenossenschaft). Einer davon muss als eingewiesener Schlüsselträger hinterlegt sein.
3.  **Arbeitszeitgesetz (ArbZG) – Ruhezeiten:** 
    - Obwohl keine Minderjährigen beschäftigt sind, gelten die gesetzlichen Ruhezeiten (11 Stunden Ruhezeit zwischen Feierabend und nächstem Dienstbeginn). Das System muss Überschneidungen (z.B. Spätschicht bis 22:30 Uhr und Frühschicht am nächsten Tag um 10:00 Uhr – hier sind 11,5 Stunden, das ist okay, aber Prüfung ist Pflicht).
    - Maximale tägliche Arbeitszeit von 10 Stunden (bei Überschreitung zwingende Ausgleichsruhe).

---

## 4. Zentrale Ist-Probleme (Schwachstellenanalyse)

Die folgenden operativen Schwierigkeiten sind der Hauptgrund für dieses Projekt:

| ID | Problemstellung | Auswirkung |
| :--- | :--- | :--- |
| **P-01** | **Externe Job-Kollisionen:** Die Verfügbarkeit der 4 Teilzeitkräfte und des 1 Minijobbers ändert sich wöchentlich, da deren *anderer Arbeitgeber* die Schichten spontan anpasst. Der Filialleiter hat keinerlei Einsicht in diese Fremdpläne und erstellt den Dienstplan "ins Blaue hinein". | Ständige, nervenaufreibende Ad-hoc-Umplanungen, bei denen der Filialleiter mitten im Tagesgeschäft anrufen und betteln muss, weil zwei Leute gleichzeitig fehlen. |
| **P-02** | **Unregelmäßige & isolierte Planverteilung:** Der aktuelle Plan wird nicht zu einem festen Stichtag veröffentlicht. Der Filialleiter versendet den fertigen Plan per WhatsApp – allerdings **an jeden Mitarbeitenden einzeln** und **an völlig zufälligen Wochentagen** (mal Dienstag, mal Donnerstagabend). | Die Mitarbeitenden können ihr Privatleben nicht planen. Es kommt regelmäßig zu Missverständnissen, weil jemand die Nachricht übersieht oder der Filialleiter vergisst, eine Einzelperson zu benachrichtigen. |
| **P-03** | **Fehlende Urlaubs-/Tauschübersicht:** Urlaubswünsche gehen weiterhin per Zettel oder Sprachnachricht ein. Es gibt keine zentrale Datenbank. | Der Filialleiter gewährt unwissentlich doppelte Urlaubsanträge für denselben Tag oder vergisst genehmigte Freizeit bei der Schichtplanerstellung. |
| **P-04** | **Überlastung der Stammkräfte:** Da die Planung unsicher ist, fragt der Filialleiter reflexartig immer die gleichen zwei Vollzeitkräfte für samstägliche Spätschichten an. | Gefahr der Unzufriedenheit und Kündigung der zuverlässigsten Mitarbeiter. |

---

## 5. Anforderungen an die zu entwickelnde Lösung (Lastenheft-Kern)

Die zu entwickelnde Software (Web-App oder Mobile-First) muss folgende **funktionale Anforderungen** erfüllen:

### 5.1 Kollisionsprüfung mit externen Jobs
- **F-01:** Die App muss eine wöchentliche "Verfügbarkeitsabfrage" ermöglichen, bei der die PT- und MJ-Mitarbeitende ihre **fremden Arbeitszeiten (externer Job)** für die kommende Woche eintragen (z.B. Mo 14-18 Uhr bei Lieferando). 
- **F-02:** Bei der automatischen Planerstellung darf das System diese externen Blöcke als **"gesperrt"** markieren und keinesfalls einen Subway-Dienst overlapping ansetzen.

### 5.2 Standardisierte Planerstellung & Verteilung
- **F-03:** Der Plan muss **spätestens immer Mittwoch um 18:00 Uhr** für die Folgewoche (Montag–Sonntag) final vom Filialleiter freigegeben werden können.
- **F-04:** Das System muss für jeden Mitarbeitenden automatisch eine **individuelle Zusammenfassung** (Datum, Uhrzeit, Rolle) generieren.
- **F-05 (Pflicht):** Die Software muss den Plan **nicht** über eine öffentliche Gruppe, sondern weiterhin **individuell** versenden können – jedoch zentralisiert. Ideal: Export als PDF/Textblock, den der Leiter per WhatsApp als Einzelchat versendet (oder native Integration via WhatsApp Business API, wenn budgetär möglich). Der *Versandtag* darf nicht mehr zufällig sein, sondern wird durch die Freigabe getriggert.

### 5.3 Urlaubs- und Tauschmanagement
- **F-06:** Digitale Erfassung von Urlaubsanträgen mit automatischem Status (Beantragt / Genehmigt / Abgelehnt).
- **F-07:** Bei der automatischen Vorschlagsberechnung muss das System eine "Verfügbarkeitsampel" (Rot/Gelb/Grün) für jeden Tag anzeigen, sodass der Leiter sofort sieht, wer noch Kapazitäten hat, um die gleichen zwei Leute nicht übermäßig zu belasten (Lastenverteilung).

### 5.4 Einhaltung der Hard Facts (automatische Prüfung)
- **F-08:** Das System darf eine Schichtplan-Freigabe **blockieren**, wenn zu einer Rushhour weniger als 4 Personen eingeplant sind.
- **F-09:** Das System darf eine Schichtplan-Freigabe **blockieren**, wenn beim Closing weniger als 2 Personen eingetragen sind.

---

## 6. Nicht-funktionale Anforderungen

| Bereich | Anforderung |
| :--- | :--- |
| **Zugriff** | Zugang erfolgt rollenbasiert (1x Admin/Filialleiter, 10x Mitarbeiter). |
| **Datenschutz (DSGVO)** | Da sensible Arbeitszeiten und externe Job-Daten verarbeitet werden, muss die Software auf deutschen/europäischen Servern hosten und eine Verschlüsselung der personenbezogenen Daten gewährleisten. |
| **Usability** | Die Oberfläche muss so intuitiv sein, dass sie auf dem Smartphone (primäres Endgerät der Mitarbeiter) ohne Einarbeitung bedienbar ist. |
| **Verfügbarkeit** | Das System muss zu den Stoßzeiten (Sonntagabend/Montagmorgen) stabil laufen, da dann viele Mitarbeiter ihre Fremdverfügbarkeit nachtragen. |

---

## 7. Abnahmekriterien (Definition of Done)

Das Projekt gilt als erfolgreich abgenommen, wenn folgende Szenarien im Praxistest (4 Wochen Pilotphase) fehlerfrei laufen:

1.  Der Filialleiter erstellt einen Plan innerhalb von **maximal 20 Minuten** (bisher 2–3 Stunden).
2.  Eine Teilzeitkraft trägt am Sonntag ihren externen Job für den kommenden Donnerstag ein; der generierte Plan weist für diesen Zeitraum *keine* Subway-Schicht auf.
3.  Der wöchentliche Plan wird zuverlässig **jeden Mittwoch** bis 18:00 Uhr verschickt – ohne dass der Filialleiter manuell fünf verschiedene Chats durchsuchen muss.
4.  Die "gleichen zwei Samstags-Schichten" wurden im Testzeitraum auf mindestens 4 verschiedene Mitarbeiter verteilt, da die Ampel-Funktion dem Leiter Alternativen vorschlägt.
5.  Es kommt zu keiner einzigen ungeplanten Unterschreitung der 4-Mann-Rushhour.

---

*Dieses Lastenheft bildet die verbindliche Grundlage für die anschließende Angebotsphase und die technische Umsetzung. Änderungen bedürfen der beidseitigen schriftlichen Zustimmung.*
