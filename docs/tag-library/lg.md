# `<lg/>` (Gruppe von Vers(zeil)en)

**Modul:** Kernmodule

## Beschreibung

enthält eine oder mehrere Verse bzw. Verszeilen, die zusammen eine formale Einheit (z. B. Strophe, Refrain) bilden.

## Erläuterung

enthält lediglich Vers(zeil)en (l) oder verschachtelte Gruppen von Vers(zeil)en
      (lg); eine Überschrift ist fakultativ.

Ausführliche Dokumentation:

- [Textstruktur > Gedichte](https://dokumentation.karl-barth.ch/textstruktur/gedichte/)

## Erlaubt in

**Kernmodule:** [`<head>`](head.md), [`<lg>`](lg.md), [`<sp>`](sp.md)

## Inhaltsmodell

- [`<lg>`](lg.md)
- [`<lg>`](lg.md)
- *model.divTop*
- *model.global*
- *model.lLike*
- *model.stageLike*
- *model.labelLike*
- *model.pPart.transcriptional*
- *model.lLike*
- *model.stageLike*
- *model.labelLike*
- *model.pPart.transcriptional*
- *model.global*
- *model.divBottom*
- *model.global*

## Constraints

**atleast1oflggapl**
:   An lg element must contain at least one child l, lg, or gap element.

**abstractModel-structure-lg-in-l**
:   Abstract model violation: Lines may not contain line groups.
