# `<p/>` (Absatz)

**Modul:** Kernmodule

## Beschreibung

Absatz. Darf nicht verschachtelt werden (ausser innerhalb von note).

!!! note "Ausführliche Dokumentation"
    [Textstruktur > Absatz](https://dokumentation.karl-barth.ch/textstruktur/absatz/)


## Inhaltsmodell

- *macro.paraContent*

## Constraints

**p1**
:   p1: p darf nicht in p vorkommen (Ausnahme in note).

**abstractModel-structure-p-in-ab-or-p**
:   Abstract model violation: Paragraphs may not occur inside other paragraphs or ab elements.

**abstractModel-structure-p-in-l**
:   Abstract model violation: Metrical lines may not contain higher-level structural elements such as div, p, or ab, unless p is a child of figure or note, or is a descendant of floatingText.
