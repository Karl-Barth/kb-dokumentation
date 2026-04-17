# `<list>`
*Liste*

enthält eine Reihe von Listenpunkten, die als Liste organisiert sind.

!!! note "Dokumentation"
    - [Listen](https://dokumentation.karl-barth.ch/textstruktur/listen/)

**Modul:** core

## Attribute

| Attribut | Beschreibung | Werte |
|----------|-------------|-------|
| `@type` | beschreibt die Art der Listenpunkte. | `gloss`, `index`, `instructions`, `litany`, `syllogism` (erweiterbar) |

### `@type`

- **`gloss`**: jeder Listenpunkt erläutert einen Begriff oder ein Konzept, das von einem voranstehenden label-Element genannt wird.
- **`index`**: jeder Listenpunkt ist ein Registereintrag z. B. in einem alphabetisch geordneten 
                Sachregister am Ende einer Druckausgabe.
- **`instructions`**: jeder Listenpunkt ist ein Arbeitsschritt in einer Folge von Anweisungen, 
                wie z. B. in einem Rezept.
- **`litany`**: jeder Listenpunkt ist Teil einer Reihenfolge von Gebeten, Bitten oder Anrufungen die 
                üblicherweise in einem religiösen Ritual verwendet werden.
- **`syllogism`**: jeder Listenpunkt ist Teil eines Arguments, das aus zwei oder mehr Prämissen 
                und einem daraus gezogenen Schluss besteht.

## Content-Model

model.divTop, model.global, `<desc>`, `<item>`, model.global, `<headLabel>`, `<headItem>`, `<label>`, model.global, `<item>`, model.global, model.divBottom, model.global

## Constraints

- **gloss-list-must-have-labels**: The content of a "gloss" list should include a sequence of one or more pairs of a label element followed by an item element
