#Relationale Datenbanken

##Infos
http://de.wikipedia.org/wiki/Relationale_Datenbank

##Grundwissen

Vereinfacht ausgedrückt bestehen relationale Datenbanken aus Tabellen, in denen Daten
gespeichert sind. Üblicherweise stehen die Tabellen in Beziehungen zueinander, d. h. manche
Einträge sind Verweise auf andere Einträge in anderen Tabellen.

###Anforderungen an eine Datenbank
 
 - _geringe Redundanz_: Nach Möglichkeit sind gleiche Daten nicht an gleiche Stellen abgelegt. Dadurch wird Speicherplatz gespart und Updates der Daten weden erleichtert.
 - _Gute Handhabbarkeit, einfache Zugriffe über möglichst wenige_: Daten sind übersichtlich abgelegt und Abfragen der Daten sind einfach.
 - _Konsitenz und Integrität_: Datenbeziehungen bleiben logisch und stimmit. Reduzierte Gefahr von Datenverlust z.B. durch Updates oder Löschen.

##Ein Beispiel - wie es nicht gemacht werden sollte

Eine Tabelle abgesetzten Produkten nach Verkäufer (_Tabelle 1_):

Verk_nr | Verk_name | PLZ | Verk_adresse | Produktname | Umsatz
--- | --- | --- | --- | --- | ---
V1 | Meier | 80075 | München | PC | 1200
V1 | Meier | 80075 | München | Laptop | 800
V1 | Meier | 80075 | München | Drucker | 300
V2 | Schneider | 70038 | Stuttgard | Laptop | 800
V2 | Schneider | 70038 | Stuttgard | Drucker | 300
V3 | Müller | 10183 | Berlin | Monitor | 1200

Zu jedem Verkäufer ist 
 1. dessen Nummer und Name (*Verk_Nr* und *Verk_Name*),
 2. die PLZ und di Stadt seiner Adresse (*PLZ* und *Verk_Adresse*), 
 3. der Name der von ihm verkauften Produkte (*Produktname*)
 4. und der *Umsatz* angegeben.

###Nachteile in _Tabelle 1_

 - Redundanzen: Name, PLZ und die Adresse der Verkäufer kommen mehrfach vor.
 - Unbequeme Handhabbarkeit: ändert ein beliebiger Verkäufer seine Adresse, so ist eine variable Anzahl von Adresseinträgen zu ändern. Falls nicht alle Adresseinträge geändert werden, so besteht die Gefahr von Inkonsistenzen

###Das große Problem von Redundanzen!
Redundanz ist immer eine Gefahrenquelle für Fehler und Inkonsistenzen.
Falls die Firma den Artikel Staubsauger aus dem Programm nimmt, so können nicht einfach die Zeilen, die den Produktnamen Monitor enthalten, entfernt werden, da sonst auch alle Informationen zu Verkäufer Müller aus der Datenbank entfernt werden!

##Die Datenbank Tabelle - Relationale Datenstrukturen

Eine Datenbank besteht aus einer oder mehreren Datenbaktabellen, in der Fachsprache auch Relation (engl. f. Beziehung) genannt.

###Fachbegriffe in alltägliche Begriffe im Vergeleich

 - **Relationenname**: _Der Name eine Datenbanktabelle_
 - **Attribut**: _eine Spalte, ein Feld einer Tabelle_
 - **Relationenschema**: _Der Tabellenkopf_
 - **Relation**: _(Datenbank)Tabelle_
 - **Tupel**: _eine Zeile (Reihe) einer Tabelle_
 - **Wert**: _Der Wert eine Zeile_
 - **Kardinalität**: _Anzahl der Zeilen einer Tabelle_
 - **Grad**: _Anzahl der Tabellen einer Spalte_
 - **Primärschlüssel**: _*eindeutiger* Bezeichner einer Zeile (Tupel)_ (Siehe _Tabelle 1_ *Verk_nr*)

###[ein Schaubild](http://upload.wikimedia.org/wikipedia/commons/thumb/1/1b/Begriffe_relationaler_Datenbanken.svg/800px-Begriffe_relationaler_Datenbanken.svg.png)
