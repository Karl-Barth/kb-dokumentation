# `<stage>`
*Regieanweisung*

enthält jegliche Regieanweisung in einem Dramentext oder -fragment.

**Modul:** core

## Attribute

| Attribut | Beschreibung | Werte |
|----------|-------------|-------|
| `@type` | beschreibt die Art der Regieanweisung. | `setting`, `entrance`, `exit`, `business`, `novelistic`, `delivery`, `modifier`, `location`, `mixed` (erweiterbar) |

### `@type`

- **`setting`**: beschreibt die Szenerie.
- **`entrance`**: beschreibt einen Auftritt.
- **`exit`**: beschreibt einen Abgang.
- **`business`**: beschreibt eine Bühnenhandlung.
- **`novelistic`**: beschreibt eine narrative Regieanweisung.
- **`delivery`**: beschreibt die Art und Weise der Darbietung einer Figurenrede.
- **`modifier`**: gibt nähere Details zu einer Figur an.
- **`location`**: beschreibt einen Handlungsort.
- **`mixed`**: mehrere der oben angeführten Funktionen.

## Content-Model

macro.specialPara
