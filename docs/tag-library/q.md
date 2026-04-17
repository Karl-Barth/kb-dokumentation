# `<q>` in Anführungszeichen

Direkte Rede oder Zitat im Fliesstext.

Siehe [Textstruktur > Gedichte](https://dokumentation.karl-barth.ch/textstruktur/gedichte/)

**Modul:** core — Kernmodule

## Attribute

**att.global** stellt gemeinsame Attribute für alle Elemente im TEI-Kodierungsschema bereit.

**@xml:id** (optional)
:   liefert einen Identifikator für das Element, welches dieses Attribut trägt.
:   Datentyp: ID

**@n** (optional)
:   gibt eine Nummer (oder eine andere Bezeichnung) für ein Element an, die innerhalb des Dokuments nicht zwangsläufig eindeutig ist.
:   Datentyp: teidata.text

**@xml:lang** (optional)
:   gibt die Sprache des Elementinhalts durch ein Tag an, das nach BCP 47 festgelegt wird.
:   Datentyp: teidata.language

**@xml:base** (optional)
:   liefert eine Basis-URI-Referenz, mit der Anwendungen relative URI-Referenzen in absolute auflösen können.
:   Datentyp: teidata.pointer

**@xml:space** (optional, geschlossene Werteliste)
:   signalisiert die gewünschte Handhabung von Leerzeichen durch Anwendungen.
:   Datentyp: teidata.enumerated
:   `default`
:   `preserve`


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


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


## Enthalten in

**core:** [cit](cit.md) "Zitat mit optionaler bibliographischer Angabe." [sp](sp.md) "enthält eine einzelne Figurenrede in einem Dramentext oder e"

## Content Model

```xml
<content>
  <macroRef key="macro.specialPara"/>
</content>
```
