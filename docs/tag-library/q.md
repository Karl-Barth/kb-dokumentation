# `<q>` in Anführungszeichen

Direkte Rede oder Zitat im Fliesstext.

Siehe [Textstruktur > Gedichte](https://dokumentation.karl-barth.ch/textstruktur/gedichte/)

[TEI Guidelines: q](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-q.html)

**Modul:** core — Kernmodule

## Attribute

**@type** (optional, erweiterbar)
:   kann verwendet werden, um anzuzeigen, ob die abgesetzte 
        Textpassage gesprochen oder gedacht wird, oder um sie auf andere Weise detaillierter zu beschreiben.
:   Datentyp: teidata.enumerated
:   `spoken` — Wiedergabe gesprochener Sprache
:   `thought` — Wiedergabe von Gedanken, z. B. eines inneren Monologes
:   `written` — Zitat aus einer schriftlichen Quelle
:   `soCalled` — Distanzierung des Autors
:   `foreign`
:   `distinct` — linguistisch hervorgehoben
:   `term` — Fachbegriff
:   `emph` — rhetorische Emphase
:   `mentioned` — bezieht sich auf sich selbst, 
            nicht auf den üblichen Bezugspunkt

**@rend** (optional)

**@xml:lang** (optional)


## Enthalten in

**core:** [cit](cit.md) "Zitat mit optionaler bibliographischer Angabe." [sp](sp.md) "enthält eine einzelne Figurenrede in einem Dramentext oder e"

## Content Model

```xml
<content>
  <macroRef key="macro.specialPara"/>
</content>
```
