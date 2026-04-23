# `<text>`

enthält einen einzelnen, eigenständigen oder kompilierten Text, zum Beispiel ein Gedicht oder
    Drama, eine Sammlung von Aufsätzen, einen Roman, ein Wörterbuch oder ein Korpus-Sample.

Dieses Element sollte nicht benutzt werden, um einen Text wiederzugeben, der an irgendeiner
      Stelle in einer anderen Struktur eingefügt ist, wie z. B. eine eingebettete oder zitierte
      Erzählung. Für diesen Zweck wird das Element floatingText benutzt.

[TEI Guidelines: text](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-text.html)

**Modul:** textstructure — Textstruktur

## Attribute

**@xml:lang** (optional)


## Enthalten in

**textstructure:** [TEI](TEI.md) "enthält ein einzelnes TEI-konformes Dokument, das aus einem "

## Kann enthalten

**textstructure:** [body](body.md) "Enthält den gesamten Textkörper eines KBGA-Dokuments."

**core:** [lb](lb.md) "markiert den Anfang einer neuen typographischen 
    Zeile i" [milestone](milestone.md) "markiert einen Grenzpunkt, der Abschnitte eines Textes trenn" [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [pb](pb.md) "Seitenumbruch. Das @ed unterscheidet die Ausgabe (pga, A), @"

**linking:** [anchor](anchor.md) "Ankerpunkt für Querverweise (@type='cross') und für Fussnote"

**figures:** [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik ("

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
"

**analysis:** [span](span.md) "associates an interpretative annotation directly with a span"

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
