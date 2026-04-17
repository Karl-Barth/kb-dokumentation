# `<p>` Absatz

Absatz. Darf nicht verschachtelt werden (ausser innerhalb von note).

Siehe [Textstruktur > Absatz](https://dokumentation.karl-barth.ch/textstruktur/absatz/)

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


**att.declaring** provides attributes for elements which may be independently associated with a particular declarable element within the header, thus overriding the inherited default for that element.

**@decls** (optional)
:   Datentyp: teidata.pointer


## Constraints

**p1**
:   p1: p darf nicht in p vorkommen (Ausnahme in note).

**abstractModel-structure-p-in-ab-or-p**
:   Abstract model violation: Paragraphs may not occur inside other paragraphs or ab elements.

**abstractModel-structure-p-in-l**
:   Abstract model violation: Metrical lines may not contain higher-level structural elements such as div, p, or ab, unless p is a child of figure or note, or is a descendant of floatingText.

## Beispiele

```xml
<p>Gottes Gebot geht mich an, sofern ich als Christ ein Glied
  seines auserwählten Volkes bin.</p>
```

## Content Model

```xml
<content>
  <macroRef key="macro.paraContent"/>
</content>
```
