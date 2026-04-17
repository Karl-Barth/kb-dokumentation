# `<change>` Änderung

Änderungsvermerk in der revisionDesc. Enthält Zeitstempel der letzten Header-Generierung.

Das who-Attribut kann dafür verwendet werden, um zu einem beliebigen anderen 
      Element zu verweisen, sollte aber typischerweise auf ein respStmt- oder 
      person-Element innerhalb des TEI-Headers zeigen, um die für die Änderungen 
      Verantwortlichen und deren Rolle zu identifizieren.
    Es wird empfohlen, Änderungen so aufzuzeichnen, dass die neuesten am Anfang eingetragen werden. 
      Das status-Attribut kann dafür verwendet werden, 
      um den Zustand des Dokuments nach erfolgter Änderung zu beschreiben.

**Modul:** header — Header

## Attribute

**att.datable** provides attributes for normalization of elements
    that contain dates, times, or datable events.

**@period** (optional)
:   Datentyp: teidata.pointer


**@target** (optional)
:   verweist auf ein oder mehrere Elemente, die zu dieser Änderung gehören.
:   Datentyp: teidata.pointer


## Enthalten in

**header:** [revisionDesc](revisionDesc.md) "dokumentiert die Änderungen, die an der Datei vorgenommen wu"

## Content Model

```xml
<content>
  <macroRef key="macro.specialPara"/>
</content>
```
