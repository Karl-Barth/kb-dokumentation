# `<persName/>`

**Modul:** Namen und Daten

## Beschreibung

Personenname mit Verweis auf die Meta-DB via @ref (kbga-actors-ID). Das @key kann provisorisch eine normalisierte Schreibweise enthalten.

## Erläuterung

Ausführliche Dokumentation:

- [Textelemente > Akteure](https://dokumentation.karl-barth.ch/textelemente/akteure/)

## Inhaltsmodell

- *macro.phraseSeq*

## Attribute

### `@ref` (optional)

Enthält eine ID aus der Meta-DB (https://kbga.karl-barth.ch)

**Datentyp:** string — Pattern: `(kbga-actors-\d+ ?)+`

### `@key` (optional)

Enthält eine normalisierte Schreibweise. Sollte nur provisorisch genutzt werden und durch ein @ref ersetzt werden
