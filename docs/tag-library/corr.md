# `<corr>`
*Korrektur*

Korrektur eines Fehlers in der Druckausgabe. Der @type unterscheidet inhaltliche Korrekturen (corr), Druckfehler (misprint) und veraltete Angaben (update).

!!! note "Dokumentation"
    - [Korrektionen Der Druckausgabe](https://dokumentation.karl-barth.ch/textelemente/korrektionen-der-druckausgabe/)

**Modul:** core

## Attribute

| Attribut | Beschreibung | Werte |
|----------|-------------|-------|
| `@type` |  | `corr`, `misprint`, `update` (geschlossen) |

### `@type`

- **`corr`**: korrigiert einen inhaltlichen Fehler
- **`misprint`**: korrigiert einen Druckfehler
- **`update`**: wenn Angaben veraltet sind, z.B. URLs

## Content-Model

macro.paraContent
