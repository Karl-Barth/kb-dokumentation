# `<text>`

enthält einen einzelnen, eigenständigen oder kompilierten Text, zum Beispiel ein Gedicht oder
    Drama, eine Sammlung von Aufsätzen, einen Roman, ein Wörterbuch oder ein Korpus-Sample.

Dieses Element sollte nicht benutzt werden, um einen Text wiederzugeben, der an irgendeiner
      Stelle in einer anderen Struktur eingefügt ist, wie z. B. eine eingebettete oder zitierte
      Erzählung. Für diesen Zweck wird das Element floatingText benutzt.

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


**att.declaring** provides attributes for elements which may be independently associated with a particular declarable element within the header, thus overriding the inherited default for that element.

**@decls** (optional)
:   Datentyp: teidata.pointer


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


## Kann enthalten

**textstructure:** [body](body.md) "Enthält den gesamten Textkörper eines KBGA-Dokuments."

## Beispiele

```xml
<text>
    <front>
      <!-- Vorspann für die gesamte Gruppierung -->
    </front>
    <group>
      <text>
        <!-- erster Text -->
      </text>
      <text>
        <!-- zweiter Text -->
      </text>
    </group>
  </text>
```

## Content Model

```xml
<content>
    <sequence>
      <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
      <sequence minOccurs="0">
        <elementRef key="front"/>
	<classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
      </sequence>
      <alternate>
        <elementRef key="body"/>
        <elementRef key="group"/>
      </alternate>
      <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
      <sequence minOccurs="0">
        <elementRef key="back"/>
	<classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
      </sequence>
    </sequence>
  </content>
```
