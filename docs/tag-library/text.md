# `<text>`

enthält einen einzelnen, eigenständigen oder kompilierten Text, zum Beispiel ein Gedicht oder
    Drama, eine Sammlung von Aufsätzen, einen Roman, ein Wörterbuch oder ein Korpus-Sample.

Dieses Element sollte nicht benutzt werden, um einen Text wiederzugeben, der an irgendeiner
      Stelle in einer anderen Struktur eingefügt ist, wie z. B. eine eingebettete oder zitierte
      Erzählung. Für diesen Zweck wird das Element floatingText benutzt.

**Modul:** textstructure — Textstruktur

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
