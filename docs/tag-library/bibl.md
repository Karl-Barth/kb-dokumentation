# `<bibl>` bibliografische Angabe

Bibliographische Angabe. Unterscheidet zwischen gedruckter Gesamtausgabe (pga), Alexander Street Press (asp), Quellen (source) und Liedern (song).

Siehe [Textelemente > Literatur](https://dokumentation.karl-barth.ch/textelemente/literatur/)

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


**att.canonical** provides attributes that can be used to associate a representation such as a name or title
    with canonical information about the object being named or referenced.

**@key** (optional)
:   Datentyp: teidata.text

**@ref** (optional)
:   Datentyp: teidata.pointer


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


**@type** (optional)
:   `pga` — Printed Gesamtausgabe (Ausgabe des TVZ)
:   `asp` — Alexander Street Press (digital edition)
:   `source` — Quelle für einen Text der KBGA

**@subtype** (optional, geschlossene Werteliste)
:   Angabe der Funktion einer Quelle für den edierten Text
:   `Vorlage_der_Edition`
:   `Weitere_Vorlage`
:   `Material_zum_Kontext`
:   `rkg` — Gesangsbuch der evangelisch-reformierten Kirchen der deutschsprachigen Schweiz (1952)
:   `ekg` — Deutsches Evangelisches Kirchengesangbuch (1950)
:   `erkg` — Gesangbuch für die evangelisch-reformirte Kirche der deutschen Schweiz (1891)
:   `eg` — Evangelisches Gesangsbuch Deutschlands (1993ff.)
:   `rg` — Reformiertes Gesangsbuch der deutschsprachigen Schweiz (1998)
:   `reichslieder` — Reichs-Lieder. Deutsches Gemeinschafts-Liederbuch

**@n** (optional)
:   Bezeichnung der Quelle für einen edierten Text
:   Datentyp: string — Pattern: `[A-Z][0-9]?`

**@xml:id** (optional)
:   Datentyp: ID — Pattern: `(b[\-0-9]+|pga|asp|kbga-(sources|bibls|songs|actors|places|keywords)-[0-9]+|[A-Z]\d*)`


## Kann enthalten

Beliebiger Textinhalt

## Constraints

**song1**
:   song1: bibl[@type='song'] muss @corresp enthalten.

**song2**
:   song2: bibl[@type='song'] darf keinen @subtype enthalten.

## Beispiele

```xml
<bibl xml:id="A" type="source">A (Vorlage der Edition): Bultmann, Rudolf, Rudolf Bultmann an Karl Barth, 11. Juni 1911. <ref target="https://kba.karl-barth.ch/objects/7950">KBA 9311.73</ref>.</bibl>
```

## Content Model

```xml
<content>
  <alternate minOccurs="0" maxOccurs="unbounded">
    <textNode/>
    <classRef key="model.gLike"/>
    <classRef key="model.highlighted"/>
    <classRef key="model.pPart.data"/>
    <classRef key="model.pPart.edit"/>
    <classRef key="model.segLike"/>
    <classRef key="model.ptrLike"/>
    <classRef key="model.biblPart"/>
    <classRef key="model.global"/>
  </alternate>
</content>
```
