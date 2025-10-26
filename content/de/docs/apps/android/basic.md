---
weight: 10
title: "Hauptbildschirm"
bookToc: false
---

# Hauptbildschirm

![](/app/android/main_realtime_25.png)

## Elemente

### Oben links – Legende

![](/app/android/legend_40.png)

  * Zeitbereich für das farbcodierte Alter der Blitzaktivität auf der Karte:
    * „weiß“: neueste Blitzaktivität innerhalb der letzten 10 Minuten
    * ...
    * „dunkelorange“: neueste Blitzaktivität vor 40 bis 50 Minuten
    * „dunkelrot“: neueste Blitzaktivität älter als 50 Minuten
  * Zusätzliche Informationen
    * Region 
      * Europa, Nordamerika, Asien, ...
      * Lokal, für einen begrenzten lokalen Bereich
      * Nicht angegeben bei globalen Daten
    * Rastergrundlage, z. B. „Raster: 10 km“
    * Zählschwellenwert
      * Nicht angezeigt, wenn der Schwellenwert inaktiv ist
      * Zum Beispiel „# > 5“ für einen Schwellenwert von 5
      * Es werden nur Rasterbereiche angezeigt, deren Blitzanzahl größer oder gleich dem Schwellenwert ist
  * Tippen Sie auf die Legende, um den Dialog „Schnelleinstellungen“ zu öffnen:

    ![](/app/android/quick-settings_25.png)

### Oben rechts – Menü/Verlauf

| Echtzeit | Verlauf |
|----------|---------|
| ![](/app/android/menu-realtime.png) | ![](/app/android/menu-history.png) |


  * Menü öffnen (auf Geräten ohne Menütaste)
  * Durch den Verlauf blättern
    * Der Zeitschritt kann in den Einstellungen geändert werden.
    * Kann verwendet werden, um die letzten 24 Stunden der Blitzaktivität zu durchsuchen.

### Unten links – Alarmradar

| aktiv | inaktiv |
|----------|---------|
| ![](/app/android/alarm-radar-active_40.png) | ![](/app/android/alarm-radar-inactive_40.png) |


  * Zeigt die Aktivität nach Entfernung für den aktuellen Standort
  * Erfordert
  	* Blitzdaten
  	* bekannten Standort
  	* Echtzeitmodus
  * Tippen, um die Karte auf den Standort zu zentrieren
  * Lange drücken, um eine größere Version des Alarmradars zu öffnen

### Unten rechts – Histogramm

![](/app/android/histogram_40.png)

  * Zeigt die Entwicklung der Einschlagsrate über den angegebenen Zeitraum (für die Datenregion)
  * Tippen, um auf die Region herauszuzoomen

### Karteninhalt

Die Blitzaktivität wird auf der Karte in Kacheln variabler Größe (5 km, 10 km, 25 km, 50 km, 100 km) dargestellt. Jede Kachel mit aufgezeichneter Blitzaktivität im ausgewählten Zeitraum wird entsprechend der jüngsten Aktivität innerhalb des aktuellen Intervalls eingefärbt. Die Zahlen innerhalb der Kacheln zeigen die Anzahl der Blitzereignisse, die im Bereich der Kachel während des entsprechenden Zeitintervalls aufgezeichnet wurden.

![](/app/android/main_map_data.png)

## Menü

### Einstellungen
 
Öffnet die detaillierten App-Einstellungen

### Alarme

Öffnet das Alarmradar:

![](/app/android/alarm-radar_25.png)

Die Farbcodierung der letzten Blitzaktivität wird gemäß den Informationen der Legende angezeigt.

### Anwendungsprotokoll

Zeigt einen Dialog mit dem internen Anwendungsprotokoll der App. Kann für unmittelbares Debugging verwendet werden. Erstellt eine E‑Mail, um das Protokoll zu versenden und Unterstützung zu erhalten.

### Änderungsprotokoll

Zeigt einen Dialog mit den neuesten App-Funktionen nach Versionsnummer

### Informationen

Zeigt einen Dialog mit appbezogenen Informationen.

## Kartennutzung

Operationen:

  * Doppeltippen zum Hineinzoomen
  * Zusammenziehen zum Zoomen (Pinch)
  * Wischen zum Verschieben
  * Lange drücken, um einen Standort für den manuellen Standortmodus auszuwählen
