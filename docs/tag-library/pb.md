# `<pb/>` (Seitenanfang)

**Modul:** Kernmodule

## Beschreibung

Seitenumbruch. Das @ed unterscheidet die Ausgabe (pga, A), @n die Seitenzahl.

!!! note "Ausführliche Dokumentation"
    [Textstruktur > Seitenanfang](https://dokumentation.karl-barth.ch/textstruktur/seitenanfang/)


## Inhaltsmodell

Leeres Element.

## Constraints

**pb1**
:   pb1: Attribut @n in pb[@ed='A'] beginnt mit 'p'.

**pb2**
:   pb2: pb[@ed='A'] darf kein @xml:id enthalten.

**pb3**
:   pb3: Attribut @n in pb[@ed='pga'] beginnt mit 'p'.

**pb4**
:   pb4: Ein pb muss innerhalb eines Absatzes stehen oder das erste Kind eines div sein.

**pb5**
:   pb5: Einem pb[@break='no'] darf kein Leerzeichen vorangehen oder folgen.
