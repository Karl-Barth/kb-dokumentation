# `<div>` Textabschnitt

Gliederungseinheit eines Textes. Der @type unterscheidet Textsorten (letter, sermon, speech etc.) und Strukturteile (opener, closer, abstract, songs).

Siehe [Textstruktur > Gliederung](https://dokumentation.karl-barth.ch/textstruktur/gliederung/)

[TEI Guidelines: div](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-div.html)

**Modul:** textstructure — Textstruktur

## Attribute

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

**@rend** (optional)

**@xml:id** (optional)

**@xml:lang** (optional)


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
