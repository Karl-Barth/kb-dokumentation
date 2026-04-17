# `<persName/>`

**Modul:** Namen und Daten

## Beschreibung

Personenname mit Verweis auf die Meta-DB via @ref (kbga-actors-ID). Das @key kann provisorisch eine normalisierte Schreibweise enthalten.

!!! note "Ausführliche Dokumentation"
    [Textelemente > Akteure](https://dokumentation.karl-barth.ch/textelemente/akteure/)


## Inhaltsmodell

- *macro.phraseSeq*

## Attribute

### `@ref`

Enthält eine ID aus der Meta-DB (https://kbga.karl-barth.ch)

**Datentyp:** `string `(kbga-actors-\d+ ?)+``

### `@key`

Enthält eine normalisierte Schreibweise. Sollte nur provisorisch genutzt werden und durch ein @ref ersetzt werden
