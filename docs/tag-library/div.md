# `<div>` Textabschnitt

Gliederungseinheit eines Textes. Der @type unterscheidet Textsorten (letter, sermon, speech etc.) und Strukturteile (opener, closer, abstract, songs).

Siehe [Textstruktur > Gliederung](https://dokumentation.karl-barth.ch/textstruktur/gliederung/)

**Modul:** textstructure — Textstruktur

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


**@type** (optional, erweiterbar)
:   `paper`
:   `abstract`
:   `excursus`
:   `letter`
:   `speech`
:   `session`
:   `chapter`
:   `alternative-text` — Eine andere Version eines Textes.

**@corresp** (optional)
:   Enthält eine xml:id eines korrespondierenden divs


## Constraints

**abstractModel-structure-div-in-l**
:   Abstract model violation: Metrical lines may not contain higher-level structural elements such as div, unless div is a descendant of floatingText.

**abstractModel-structure-div-in-ab-or-p**
:   Abstract model violation: p and ab may not contain higher-level structural elements such as div, unless div is a descendant of floatingText.

## Beispiele

**Beispiel 1:**

```xml
<div type="letter">
    <head>Brief Nr. 3</head>
    <opener>Lieber Herr Barth!</opener>
    <p>...</p>
    <closer>
      <salute>Mit herzlichem Gruß</salute>
      <signed>
        <persName ref="kbga-actors-512">Rudolf Bultmann</persName>
      </signed>
    </closer>
  </div>
```

**Beispiel 2:**

```xml
<div type="abstract">
    <p>Zusammenfassung des Textes...</p>
  </div>
```

## Content Model

```xml
<content>
  <sequence minOccurs="1" maxOccurs="1">
    <alternate minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.divTop"/>
      <classRef key="model.global"/>
    </alternate>
    <sequence minOccurs="0" maxOccurs="1">
      <alternate minOccurs="1" maxOccurs="1">
        <sequence minOccurs="1" maxOccurs="unbounded">
          <alternate minOccurs="1" maxOccurs="1">
            <classRef key="model.divLike"/>
            <classRef key="model.divGenLike"/>
          </alternate>
          <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
        </sequence>
        <sequence minOccurs="1" maxOccurs="1">
          <sequence minOccurs="1" maxOccurs="unbounded">
            <alternate minOccurs="1" maxOccurs="1">
              <elementRef key="schemaSpec"/>
              <classRef key="model.common"/>
            </alternate>
            <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
          </sequence>
          <sequence minOccurs="0" maxOccurs="unbounded">
            <alternate minOccurs="1" maxOccurs="1">
              <classRef key="model.divLike"/>
              <classRef key="model.divGenLike"/>
            </alternate>
            <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
          </sequence>
        </sequence>
      </alternate>
      <sequence minOccurs="0" maxOccurs="unbounded">
        <classRef key="model.divBottom"/>
        <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
      </sequence>
    </sequence>
  </sequence>
</content>
```
