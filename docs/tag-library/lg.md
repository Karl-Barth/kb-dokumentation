# `<lg>`
*Gruppe von Vers(zeil)en*

enthält eine oder mehrere Verse bzw. Verszeilen, die zusammen eine formale Einheit (z. B. Strophe, Refrain) bilden.

!!! note "Dokumentation"
    - [Gedichte](https://dokumentation.karl-barth.ch/textstruktur/gedichte/)

**Modul:** core

## Content-Model

model.divTop, model.global, model.lLike, model.stageLike, model.labelLike, model.pPart.transcriptional, `<lg>`, model.lLike, model.stageLike, model.labelLike, model.pPart.transcriptional, model.global, `<lg>`, model.divBottom, model.global

## Constraints

- **atleast1oflggapl**: An lg element must contain at least one child l, lg, or gap element.
- **abstractModel-structure-lg-in-l**: Abstract model violation: Lines may not contain line groups.
