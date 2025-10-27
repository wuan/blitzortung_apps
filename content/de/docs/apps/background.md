---
weight: 10
title: "Hintergrund und Geschichte"
bookToc: false
---

# Hintergrund und Geschichte

Die Entwicklung begann 2012 als Spaßprojekt auf Basis der Daten von [Blitzortung.org](http://blitzortung.org) mit folgenden Grundideen:

## Datenschutzüberlegungen

* Keine Werbung zur Monetarisierung der App verwenden.
* Keine Verfolgung einzelner Geräte/Nutzer.
* Keine Push-Benachrichtigungen (könnten die Privatsphäre der Nutzer beim Push-Dienst beeinträchtigen).
* Keine Quell-IP-Adressen tracken (nur eine lokale GeoIP-Datenbank zur groben Standortabschätzung verwenden).

## Anfangskonfiguration

Anfangs musste der Nutzer eine Region auswählen (Begrenzungsrahmen auf der Karte, der in etwa der von Blitzortung.org verwendeten Region entspricht).

## Einführung von Alarmen

### Gerätestandort

* Standortdaten sollten das Gerät nicht verlassen.
* Verwendung vollständiger Regionsdaten, wofür der Nutzer die Region einstellen muss, in der er sich aktuell befindet.
* Generell sind Standortdaten für den Betrieb der App nicht erforderlich.
* Der Nutzer kann auch einen manuellen Standort wählen. Dadurch sind Alarme möglich, ohne dass das Gerät den Standort des Nutzers verfolgt.

### Regelmäßige Datenaktualisierungen

* Daten für die konfigurierte Region abrufen.
* Der Hintergrundbetrieb des App-Dienstes erfordert zusätzliche Berechtigungen.
* Dies kann die Batterielaufzeit beeinträchtigen, insbesondere bei Intervallen im Bereich von 1 Minute. (Wir haben festgestellt, dass 5‑Minuten‑Intervalle ein guter Kompromiss sind.)

## Einführung des Global-/Lokaldatenmodus

Die Notwendigkeit, die richtige Region zu konfigurieren, war für unsere Nicht‑EU‑Nutzer schon immer ein Problem (die EU ist die voreingestellte Standardregion).

Um die Serverlast, den gesamten Datentransfer und die Netzwerknutzung des Geräts zu minimieren, haben wir einen Lokaldatenmodus eingeführt, der nur Daten für einen lokalen Bereich um den Gerätestandort anfordert.

Dies geschieht, indem Längen- und Breitengrad des Gerätestandorts auf 5°‑Schritte gerastert werden. Das ist grob genug, um keine bessere Verfolgung zu erlauben als über die IP‑Adresse. Übertragen werden die Daten für eine 15° × 15° große Kachel, die den Nutzerbereich umgibt, um auch am Rand der Region eine vollständige Abdeckung zu gewährleisten.

   ![](/app/background/local_data.png)

## Umstieg von Google Maps auf OpenStreetMap

April 2019 (Version 1.6.5 bis 2.0.0)

Dieser Schritt war seit einiger Zeit geplant und sollte mehrere Probleme lösen:

* Unabhängigkeit vom Google Play Store, um die App auch für Nutzer, die Google‑Dienste vermeiden möchten, bei F‑Droid bereitzustellen.
* Google Maps V1 wurde eingestellt und benötigte einen Ersatz.

Nachteil war, dass wir die (vergleichsweise dunkle) Satellitenansicht durch die standardmäßig gerenderten Kacheln von OpenStreetMap ersetzen mussten (die Entscheidung fiel gegen eine Geräterenderung, um die Nutzung auf älteren Geräten zu ermöglichen).

Anfangs hat es einige Zeit gedauert, die beste Konfiguration und Anzeigeeinstellungen (Helligkeit und Skalierung) für OpenStreetMap‑Kacheln zu finden. Dazu gehörten auch die richtigen Berechtigungen für die lokale Speicherung, um heruntergeladene Kacheln zu cachen.

Wir hatten viele unzufriedene Nutzer und erhielten zahlreiche Ein‑Stern‑Bewertungen, mit denen man uns wieder zu Google Maps drängen wollte – was aus den oben genannten Gründen keine Option war.

| ![](/app/background/gmapv1_1.6.5.png) | ![](/app/background/osm_2.0.0.png) |
|---|---|

## Einführung automatischer Rastergröße und Lokaldatenmodus

Eingeführt im Juni 2020 mit Version 2.1.0 (265)

Der Lokaldatenmodus war bereits ein großer Schritt, um den Datentransfer und die Serverlast im Hintergrundbetrieb zu minimieren. Dennoch belasteten globale Datenabfragen mit 5‑km‑Raster aus der interaktiven App‑Nutzung die Server.

Es war daher an der Zeit, eine automatische Auswahl von Rastergröße und Datenmodus für die interaktive Nutzung einzuführen, die vollständig transparent abläuft: globaler Datenmodus für kleine Zoomstufen (Welt-/Kontinent‑Übersicht) und automatisches Umschalten auf den Lokaldatenmodus, wenn Nutzer in eine bestimmte Region hineinzoomen.

## Einführung des Animationsmodus und Verlaufsreglers

Oktober 2023, Version 2.2.0 (313)

![](/app/android/main_animation.webm)

Der Animationsmodus stand lange auf unserer Wunschliste. Mit dem zusätzlichen Caching‑Mechanismus ist es möglich, einen Zeitschieberegler für den Verlauf zu implementieren, der direkten Zugriff auf vergangene Daten erlaubt.

## Interne Modernisierung

August 2025, Version 2.4.0 (341)

Mit der zunehmenden Komplexität des modernen Android‑Berechtigungsmanagements haben wir die Berechtigungslogik und den zugehörigen Code vollständig neu geschrieben, die zuvor bereits zu Problemen für unsere Nutzer geführt hatten.


