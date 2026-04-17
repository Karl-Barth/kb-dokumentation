# `<anchor>`
*Ankerpunkt*

Ankerpunkt für Querverweise (@type='cross') und für Fussnoten mit mehreren Fussnotenzeichen (@type='note').

!!! note "Dokumentation"
    - [Anmerkungen](https://dokumentation.karl-barth.ch/textstruktur/anmerkungen/)
    - [Querverweise](https://dokumentation.karl-barth.ch/textelemente/querverweise/)

**Modul:** linking

## Attribute

| Attribut | Beschreibung | Werte |
|----------|-------------|-------|
| `@type` | Wird für Querverweise und für Fussnoten verwendet, die im Text mehrere Fussnotenzeichen haben. | `cross`, `note` (geschlossen) |

### `@type`

- **`cross`**: Anker für Querverweis
- **`note`**: Stelle für zweites Fussnotenzeichen; in der note/@target wird die @xml:id gesetzt

## Content-Model

(leer)
