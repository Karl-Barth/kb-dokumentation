# `<head>` Überschrift

Überschrift einer Gliederungseinheit (div).

Siehe [Textstruktur > Ueberschriften](https://dokumentation.karl-barth.ch/textstruktur/ueberschriften/)

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


**att.placement** provides attributes for describing where on the source page or
  object a textual element appears.

**@place** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `top`
:   `bottom`
:   `margin`
:   `opposite`
:   `overleaf`
:   `above`
:   `right`
:   `below`
:   `left`
:   `end`
:   `inline`
:   `inspace`


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


## Kann enthalten

Beliebiger Textinhalt

**core:** [lg](lg.md) "enthält eine oder mehrere Verse bzw. Verszeilen, die zusamme"

## Beispiele

**Beispiel 1:**

```xml
<div1 n="I" type="book">
    <head>In the name of Christ here begins the first book of the ecclesiastical history of
          Georgius Florentinus, known as Gregory, Bishop of Tours.</head>
    <div2 type="section">
      <head>In the name of Christ here begins Book I of the history.</head>
      <p>Proposing as I do ...</p>
      <p>From the Passion of our Lord until the death of Saint Martin four hundred and twelve
            years passed.</p>
      <trailer>Here ends the first Book, which covers five thousand, five hundred and ninety-six
            years from the beginning of the world down to the death of Saint Martin.</trailer>
    </div2>
  </div1>
```

**Beispiel 2:**

```xml
With a few exceptions, connectives are equally
      useful in all kinds of discourse: description, narration, exposition, argument.
<list rend="bulleted">
  <head>Connectives</head>
  <item>above</item>
  <item>accordingly</item>
  <item>across from</item>
  <item>adjacent to</item>
  <item>again</item>
  <item>
    <!-- ... -->
  </item>
</list>
```

## Content Model

```xml
<content>
  <alternate minOccurs="0" maxOccurs="unbounded">
    <textNode/>
    <elementRef key="lg"/>
    <classRef key="model.gLike"/>
    <classRef key="model.phrase"/>
    <classRef key="model.inter"/>
    <classRef key="model.lLike"/>
    <classRef key="model.global"/>
  </alternate>
</content>
```
