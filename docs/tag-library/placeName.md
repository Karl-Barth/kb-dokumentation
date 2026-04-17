# `<placeName/>`

**Modul:** Namen und Daten

## Beschreibung

Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-ID). Das @key kann provisorisch eine normalisierte Schreibweise enthalten.

## Erläuterung

Ausführliche Dokumentation:

- [Textelemente > Orte](https://dokumentation.karl-barth.ch/textelemente/orte/)

## Inhaltsmodell

- *macro.phraseSeq*

## Attribute

### `@ref` (optional)

Enthält eine ID aus der Meta-DB (https://kbga.karl-barth.ch)

**Datentyp:** string — Pattern: `(kbga-places-\d+ ?)+`

### `@key` (optional)

Enthält eine normalisierte Schreibweise. Sollte nur provisorisch genutzt werden und durch ein @ref ersetzt werden

## Beispiele

```xml
<placeName ref="kbga-places-41">Marburg</placeName>
```
