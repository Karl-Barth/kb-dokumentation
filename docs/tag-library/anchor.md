# `<anchor/>` (Ankerpunkt)

**Modul:** Linking

## Beschreibung

Ankerpunkt für Querverweise (@type='cross') und für Fussnoten mit mehreren Fussnotenzeichen (@type='note').

!!! note "Ausführliche Dokumentation"
    [Textstruktur > Anmerkungen](https://dokumentation.karl-barth.ch/textstruktur/anmerkungen/)

    [Textelemente > Querverweise](https://dokumentation.karl-barth.ch/textelemente/querverweise/)


## Inhaltsmodell

Leeres Element.

## Attribute

### `@type` (geschlossene Werteliste)

Wird für Querverweise und für Fussnoten verwendet, die im Text mehrere Fussnotenzeichen haben.

**Mögliche Werte:**

- `cross` — Anker für Querverweis
- `note` — Stelle für zweites Fussnotenzeichen; in der note/@target wird die @xml:id gesetzt
