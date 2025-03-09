## Verwaltung/Admin

- Die Verwaltung ist für das Anlegen und Verwalten von Benutzerkonten und die Verwaltung der Rechte dieser verantwortlich.

### *Anlegen Nutzerkonto -> in Verwaltungsuebersicht*

**1. Use-Case: "Standortleitung erstellen"**

**2. Use-Case: "Gruppenleitung erstellen"**


## Standortleitung

**3. Use-Case: "Vertretung zuweisen"**
- Die Standortleitung hat eine Übersicht über alle Gruppen in ihrer Werkstatt. 
    Sie verwaltet die Einstellungen, welche Gruppenleitung als Vertretung für eine andere eingetragen wird.

- Die Standortleitung kann bei Bedarf Vertretungen für die Gruppenleitung zuweisen, 
    die es der Stellvertretung ermöglicht, die Essensbestellungen für die zu vertretenden Gruppen durchzuführen.

**4. Use-Case: "Küchenleitung erstellen und Vertretung zuweisen"**

**5. Use-Case: "Mitarbeiter mit QR-Code erstellen und Gruppe zuweisen"**

- Beim Anlegen einer Person mit Behinderung soll außerdem automatisch ein QR-Code erstellt werden, 
    welcher lediglich eine ID für die Person codiert und bei der Essensausgabe mit dem Tablet des Küchenpersonals ausgelesen werden kann.

## Gruppenleitung

**6. Use-Case: "14 Tage im Voraus Essen bestellen"**

- Die Gruppenleitung trägt die Essensbestellungen für ihre Gruppen 14 Tage im Voraus in die
    Webanwendung ein. 
    Pro Tag stehen zwei warme Speisen (rot und blau) sowie ein optionaler Salat zur Auswahl.

**7. Use-Case: "Essensbestellung anpassen"**    
- Die Gruppenleitung kann Bestellungen bis 8:00 Uhr des aktuellen Tages anpassen, um kurzfristige Änderungen oder Ereignisse zu berücksichtigen. 
- Nach 8:00 Uhr sind keine Änderungen mehr möglich. 
- Jede Gruppenleitung erhält nur eine Übersicht über die Mitglieder der eigenen Gruppe, außer bei Vertretungen. 
- In diesem Fall erhält ein Gruppenleiter auch die Übersicht der zu vertretenden Gruppe und ist in der Lage, die Essensbestellungen für diese Gruppe aufzunehmen.

## Kuechenpersonal

**8. Use-Case: "Anmeldung Küchenpersonal-Gruppenleitung ohne doppelten Login"** 

- Eine Person des Küchenpersonals übernimmt außerdem die Rolle der Gruppenleitung und sollte die entsprechenden Rechte ohne doppelte Anmeldung erhalten.

**9 a. Use-Case: "Essensbestellung scannen"**

- Konkret soll mithilfe der Webcam der QR-Code der Person eingescannt werden, sodass das Küchenpersonal überprüfen kann, welches Essen die Person bestellt hat. 

**9 b. Use-Case: "Doppelte Bestellungen"**

- Zudem muss durch das Einscannen des QR-Codes die Ausgabe des Essens in der Bestellung der Person vermerkt und in der Datenbank entsprechend gespeichert werden, sodass doppelte Essensausgaben für dieselbe Person vermieden werden.

Jedoch muss das Küchenpersonal zusätzlich die Möglichkeit haben, den Status der Ausgabe des Essens manuell anpassen zu können, wenn Personen bspw. keine Speisen mehr erhalten können aufgrund fehlerhafter Bestellungen.

**discarded** 

Use-Case: "Vertretung passt Essensbestellung an" 

Dementsprechend muss die Übersicht die Personen der Gruppe anzeigen sowie die Möglichkeit bieten, die Essensbestellung pro Person einzutragen.
