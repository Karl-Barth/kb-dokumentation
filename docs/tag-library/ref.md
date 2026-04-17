# `<ref>`
*Referenz*

Verweis auf eine andere Ressource. Dient für Bibelstellen, Literaturverweise, Querverweise und URLs.

!!! note "Dokumentation"
    - [Querverweise](https://dokumentation.karl-barth.ch/textelemente/querverweise/)

**Modul:** core

## Content-Model

macro.paraContent

## Constraints

- **ref1**: ref1: ref darf nicht in ref vorkommen.
- **ref2**: ref2: @target in ref[@subtype='bibl'] darf kein Komma oder Bindestrich enthalten.
- **refAtts**: Only one of the attributes @target and @cRef may be supplied on .
