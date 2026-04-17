# `<persName>`

Personenname mit Verweis auf die Meta-DB via @ref (kbga-actors-ID). Das @key kann provisorisch eine normalisierte Schreibweise enthalten.

!!! note "Dokumentation"
    - [Akteure](https://dokumentation.karl-barth.ch/textelemente/akteure/)

**Modul:** namesdates

## Attribute

| Attribut | Beschreibung | Werte |
|----------|-------------|-------|
| `@ref` | Enthält eine ID aus der Meta-DB (https://kbga.karl-barth.ch) | string ((kbga-actors-\d+ ?)+) |
| `@key` | Enthält eine normalisierte Schreibweise. Sollte nur provisorisch genutzt werden und durch ein @ref ersetzt werden |  |

## Content-Model

macro.phraseSeq
