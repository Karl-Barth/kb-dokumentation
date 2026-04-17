# `<ref/>` (Referenz)

**Modul:** Kernmodule

## Beschreibung

Verweis auf eine andere Ressource. Dient für Bibelstellen, Literaturverweise, Querverweise und URLs.

!!! note "Ausführliche Dokumentation"
    [Textelemente > Querverweise](https://dokumentation.karl-barth.ch/textelemente/querverweise/)


## Inhaltsmodell

- *macro.paraContent*

## Constraints

**ref1**
:   ref1: ref darf nicht in ref vorkommen.

**ref2**
:   ref2: @target in ref[@subtype='bibl'] darf kein Komma oder Bindestrich enthalten.

**refAtts**
:   Only one of the attributes @target and @cRef may be supplied on .
