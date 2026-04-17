# `<list/>` (Liste)

**Modul:** Kernmodule

## Beschreibung

enthält eine Reihe von Listenpunkten, die als Liste organisiert sind.

!!! note "Ausführliche Dokumentation"
    [Textstruktur > Listen](https://dokumentation.karl-barth.ch/textstruktur/listen/)


## Inhaltsmodell

- `<desc>`
- [`<item>`](item.md)
- `<headLabel>`
- `<headItem>`
- `<label>`
- [`<item>`](item.md)
- *model.divTop*
- *model.global*
- *model.global*
- *model.global*
- *model.global*
- *model.divBottom*
- *model.global*

## Attribute

### `@type` (erweiterbare Werteliste)

beschreibt die Art der Listenpunkte.

**Datentyp:** `teidata.enumerated`

**Mögliche Werte:**

- `gloss` — jeder Listenpunkt erläutert einen Begriff oder ein Konzept, das von einem voranstehenden label-Element genannt wird.
- `index` — jeder Listenpunkt ist ein Registereintrag z. B. in einem alphabetisch geordneten 
                Sachregister am Ende einer Druckausgabe.
- `instructions` — jeder Listenpunkt ist ein Arbeitsschritt in einer Folge von Anweisungen, 
                wie z. B. in einem Rezept.
- `litany` — jeder Listenpunkt ist Teil einer Reihenfolge von Gebeten, Bitten oder Anrufungen die 
                üblicherweise in einem religiösen Ritual verwendet werden.
- `syllogism` — jeder Listenpunkt ist Teil eines Arguments, das aus zwei oder mehr Prämissen 
                und einem daraus gezogenen Schluss besteht.

## Constraints

**gloss-list-must-have-labels**
:   The content of a "gloss" list should include a sequence of one or more pairs of a label element followed by an item element
