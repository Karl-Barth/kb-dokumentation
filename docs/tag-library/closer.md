# `<closer>`

Schlussformel eines Briefes (Gruss, Unterschrift, Datum).

Siehe [Textstruktur > Dateline](https://dokumentation.karl-barth.ch/textstruktur/dateline/)

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


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


## Kann enthalten

Beliebiger Textinhalt

**textstructure:** [dateline](dateline.md) "enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw." [salute](salute.md) "enthält eine Anrede oder Grußformel, die einem Vorwort, eine" [signed](signed.md) "enthält die abschließende Grußformel o.Ä. die ein Vorwort, e"

## Beispiele

```xml
<closer>
    <salute>Mit herzlichem Gruß</salute>
    <salute>Ihr</salute>
    <signed>
      <persName ref="kbga-actors-512">Rudolf Bultmann</persName>
    </signed>
  </closer>
```

## Content Model

```xml
<content>
  <alternate minOccurs="0" maxOccurs="unbounded">
    <textNode/>
    <classRef key="model.gLike"/>
    <elementRef key="byline"/>
    <elementRef key="signed"/>
    <elementRef key="dateline"/>
    <elementRef key="salute"/>
    <classRef key="model.phrase"/>
    <classRef key="model.global"/>
  </alternate>
</content>
```
