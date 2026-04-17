# `<docDate>` Datierung des Dokuments

enthält die Datierung des Dokuments, wie auf der Titelseite oder in einer Datumszeile angegeben.

Vgl. das allgemeine date-Element im core-Modul. Dieses
      spezialisierte Element erleichtert die Kodierung und Verarbeitung der Datierung eines Dokuments,
      die vermutlich in vielen Anwendungsszenarien gesondert behandelt wird. Es sollte nur für das
      Datum des gesamten Dokuments verwendet werden, nicht für Datierungen von Abschnitten oder
      Teilen.

**Modul:** textstructure — Textstruktur

## Attribute

**att.global** stellt gemeinsame Attribute für alle Elemente im TEI-Kodierungsschema bereit.

**@xml:id** (optional)
:   liefert einen Identifikator für das Element, welches dieses Attribut trägt.
:   Datentyp: ID

**@n** (optional)
:   gibt eine Nummer (oder eine andere Bezeichnung) für ein Element an, die innerhalb des Dokuments nicht zwangsläufig eindeutig ist.
:   Datentyp: teidata.text

**@xml:lang** (optional)
:   gibt die Sprache des Elementinhalts durch ein Tag an, das nach BCP 47 festgelegt wird.
:   Datentyp: teidata.language

**@xml:base** (optional)
:   liefert eine Basis-URI-Referenz, mit der Anwendungen relative URI-Referenzen in absolute auflösen können.
:   Datentyp: teidata.pointer

**@xml:space** (optional, geschlossene Werteliste)
:   signalisiert die gewünschte Handhabung von Leerzeichen durch Anwendungen.
:   Datentyp: teidata.enumerated
:   `default`
:   `preserve`


**att.calendarSystem** provides attributes for indicating calendar systems to which a date belongs.

**@calendar** (optional)
:   Datentyp: teidata.pointer


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


**att.datable** provides attributes for normalization of elements
    that contain dates, times, or datable events.

**@period** (optional)
:   Datentyp: teidata.pointer


## Enthalten in

**textstructure:** [dateline](dateline.md) "enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw."

## Content Model

```xml
<content>
    <macroRef key="macro.phraseSeq"/>
  </content>
```
