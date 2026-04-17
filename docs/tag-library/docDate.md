# `<docDate>` Datierung des Dokuments

enthält die Datierung des Dokuments, wie auf der Titelseite oder in einer Datumszeile angegeben.

Vgl. das allgemeine date-Element im core-Modul. Dieses
      spezialisierte Element erleichtert die Kodierung und Verarbeitung der Datierung eines Dokuments,
      die vermutlich in vielen Anwendungsszenarien gesondert behandelt wird. Es sollte nur für das
      Datum des gesamten Dokuments verwendet werden, nicht für Datierungen von Abschnitten oder
      Teilen.

[TEI Guidelines: docDate](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-docDate.html)

**Modul:** textstructure — Textstruktur

## Enthalten in

**textstructure:** [dateline](dateline.md) "enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw."

## Content Model

```xml
<content>
    <macroRef key="macro.phraseSeq"/>
  </content>
```
