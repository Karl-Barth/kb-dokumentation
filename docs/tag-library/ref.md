# `<ref>` Referenz

Verweis auf eine andere Ressource. Dient für Bibelstellen, Literaturverweise, Querverweise und URLs.

Siehe [Textelemente > Querverweise](https://dokumentation.karl-barth.ch/textelemente/querverweise/)

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


**att.pointing** provides a set of attributes used by all elements which point
  to other elements by means of one or more URI references.

**@target** (optional)
:   Datentyp: teidata.pointer


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


## Constraints

**ref1**
:   ref1: ref darf nicht in ref vorkommen.

**ref2**
:   ref2: @target in ref[@subtype='bibl'] darf kein Komma oder Bindestrich enthalten.

**refAtts**
:   Only one of the attributes @target and @cRef may be supplied on .

## Beispiele

**Beispiel 1:**

```xml
<ref type="pub" target="1005">Nr. 3</ref>
```

**Beispiel 2:**

```xml
<ref target="https://kba.karl-barth.ch/objects/7950">KBA 9311.73</ref>
```

**Beispiel 3:**

```xml
<ref type="can" subtype="bible" target="Röm.1.17">Röm. 1,17</ref>
```

## Content Model

```xml
<content>
  <macroRef key="macro.paraContent"/>
</content>
```
