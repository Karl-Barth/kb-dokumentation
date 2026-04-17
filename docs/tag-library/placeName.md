# `<placeName>`

Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-ID). Das @key kann provisorisch eine normalisierte Schreibweise enthalten.

!!! note "Dokumentation"
    - [Orte](https://dokumentation.karl-barth.ch/textelemente/orte/)

**Modul:** namesdates

## Attribute

| Attribut | Beschreibung | Werte |
|----------|-------------|-------|
| `@ref` | Enthält eine ID aus der Meta-DB (https://kbga.karl-barth.ch) | string ((kbga-places-\d+ ?)+) |
| `@key` | Enthält eine normalisierte Schreibweise. Sollte nur provisorisch genutzt werden und durch ein @ref ersetzt werden |  |

## Content-Model

macro.phraseSeq
