# `<span>`

associates an interpretative annotation directly with a span of text.

**Modul:** analysis — Analyse

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


**att.interpLike** provides attributes for elements which represent a formal analysis or interpretation.

**@type** (optional)
:   Datentyp: teidata.enumerated
:   `image`
:   `character`
:   `theme`
:   `allusion`

**@subtype** (optional)
:   Datentyp: teidata.enumerated

**@inst** (optional)
:   Datentyp: teidata.pointer


**att.pointing** provides a set of attributes used by all elements which point
  to other elements by means of one or more URI references.

**@target** (optional)
:   Datentyp: teidata.pointer


**@from** (optional)
:   Datentyp: teidata.pointer

**@to** (optional)
:   Datentyp: teidata.pointer


## Constraints

**target-from**
:   Only one of the attributes @target and @from may be supplied on

**targetto**
:   Only one of the attributes @target and @to may be supplied on

**tonotfrom**
:   If @to is supplied on , @from must be supplied as well

**tofrom**
:   The attributes @to and @from on  may each contain only a single value

## Content Model

```xml
<content>
    <macroRef key="macro.phraseSeq.limited"/>
  </content>
```
