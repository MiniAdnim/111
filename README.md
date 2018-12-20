# JS-Heizungsteuerung-powered-by-LOOXER
 ab hier ChangeLog // Aktuelle Version 2.0b01 (erste Beta) 28.12.2017
// Version 2.00b02 05.01.2018 - zweite Beta
//.............................Technische Coding Aenderungen (ueberfluessige log eintragungen und doppel coding entfernt)
//.............................Kein Trigger bei Aenderung von An/Abwesenheit und Feiertagen gefixt
//.............................Bei Einstellung der Duration Manuelle Temp kleiner Null wurde bei einer Thermostataenderung am Thermostat keine Rückstellung auf schedule vorgenommen
//.............................Delay Time (notwendig für alte Thermostate) nach Fensteröffnung wieder aktiviert - 2 Minuten Verzögerung nach Fensterschliessung
//.............................Sensorstatusermittlung fuer HM-Geraete verallgemeinert (keine Speziallogik mehr notwendig. Konfig in der Sensortypetab reicht aus) / logging Eintraege fuer Sensor Aenderungen hinzugefuegt
//.............................Bei Einschalten der Heizperiode wurden die Temperaturen nicht sofort auf die geplanten Temperaturen gesetzt
// Version 2.00b03 02.04.2018 -  dritte Beta
//.............................Manuelle Temperaturen werden bei Scriptstart ignoriert/zurückgesetzt
//.............................Thermostabtypetab Position 4 auf Position 8 (nach den Wandthermosteten) verschoben
//.............................NoneHMTab - Fuellen der Position 12 in Controltab falsch (mit 0 ersetzt)
//.............................Bei gleichen Zeiten im schedule von verschiedenen Räumen kam es dazu, dass nicht geschaltet wurde. Eine Zeitverzögerung eingebaut
//.............................externe Dateiausgabe bei manuellen Aenderungen hinzugefügt (writelog)
//.............................Fehler in Routine Sensor Change bei direktvernuepften Fenstersensoren beseitigt. 
//.............................Fehler bei den Subscriptions fuer Feiertage fuehrte zu Warnmeldungen, wenn kein Feiertagsadapter genutzt wurde
// Version 2.00a01 08.10.2018 - erste Alpha
//.............................Fehler bei nicht direkten Sensoren behoben: Temperatur wurde nicht abgesenkt
//.............................Raum-Statusanzeigen (Abweichungen vom Heizplan)  wurde überarbeitet - keine Datenstrukturanpassung nötig- zentrale Routine eingefügt
//.............................Routine zur Überprüfung direktverknüpfter Sensoren nicht notwendig - entfernt
//.............................Voreinstellungen Parameter für Verschlusssensoren angepasst
//.............................Raumstatus (geoeffnet oder geschlossen ) Datenpunkt je Raum eingerichtet und Logik zum Raumstatus update fuer alle Sensoren des raumes abgebildet
//.............................Sensor aufgenommen: HMW-IO-12-Sw14-DR',  'Schließerkontakt HMW' ,  wired
// Version 2.00a02 14.10.2018 - zweite Alpha
//.............................Fehler bei nicht direkten Sensoren behoben: Temperatur wurde nicht abgesenkt / Code wieder aktiviert
// Version 2.00 26.10.2018    - erste Stable
//.............................bei direkt verknuepften Sensoren wurde bei geoeffnetem Fenster ein moeglicher Schedule Wechsel nicht berüksichtig
//Version 2.10 15.12.2018......Fehler behoben nach updae auf JS 4.0.1 !fs.existsSync funktioniert nicht mehr ausgetausch mit fs.readFile
//.............................WT HmiP-BWTH hinzugefügt
//.............................Subscription fuer ICAL Profile hinzugefügt
//.............................Delay für HM Geräte gefixt und für Nicht-HM Geräte hinzugefügt
//.............................ICAL Pfad umgestellt für ICAL Adapter Version 1.7.0
//.............................ICAL- Profile mit Selection Prio für die Profil-Selektion hizugefügt - unterstützt jetzt mehrere gleichzeitig aktive ICAL Events 
//.............................Subscription für ICAL-Raumprofile und Selektion hinzugefügt (analog zu den globalen Profilen)
//.............................nach update auf JS 4.0.2 !fs.existsSync wieder aktiviert
//.............................SoftBoost Funktion hinzugefügt (analog dem HardBoost der Thermostate)
//.............................ICAL Events können jetzt in den Views aktiviert/deaktiviert werden
//.............................Manuelle Aenderungen stabilisiert 
//Version 2.1.01 18.12.........Testraum erzeugte Fehler - Entfernt
//.............................Synchen bei nicht direkt verknüpften Thermostaten wieder hergestellt (bei Absenktemperatur)
