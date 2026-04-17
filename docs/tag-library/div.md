# `<div>`
*Textabschnitt*

Gliederungseinheit eines Textes. Der @type unterscheidet Textsorten (letter, sermon, speech etc.) und Strukturteile (opener, closer, abstract, songs).

!!! note "Dokumentation"
    - [Gliederung](https://dokumentation.karl-barth.ch/textstruktur/gliederung/)

**Modul:** textstructure

## Attribute

| Attribut | Beschreibung | Werte |
|----------|-------------|-------|
| `@type` |  | `paper`, `abstract`, `excursus`, `letter`, `speech`, `session`, `chapter`, `alternative-text` (erweiterbar) |
| `@corresp` | Enthält eine xml:id eines korrespondierenden divs |  |

### `@type`

- **`alternative-text`**: Eine andere Version eines Textes.

## Content-Model

model.divTop, model.global, model.divLike, model.divGenLike, model.global, `<schemaSpec>`, model.common, model.global, model.divLike, model.divGenLike, model.global, model.divBottom, model.global

## Constraints

- **abstractModel-structure-div-in-l**: Abstract model violation: Metrical lines may not contain higher-level structural elements such as div, unless div is a descendant of floatingText.
- **abstractModel-structure-div-in-ab-or-p**: Abstract model violation: p and ab may not contain higher-level structural elements such as div, unless div is a descendant of floatingText.
