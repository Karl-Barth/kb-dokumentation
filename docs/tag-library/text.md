# `<text/>`

**Modul:** Textstruktur

## Beschreibung

enthält einen einzelnen, eigenständigen oder kompilierten Text, zum Beispiel ein Gedicht oder
    Drama, eine Sammlung von Aufsätzen, einen Roman, ein Wörterbuch oder ein Korpus-Sample.

## Erläuterung

Dieses Element sollte nicht benutzt werden, um einen Text wiederzugeben, der an irgendeiner
      Stelle in einer anderen Struktur eingefügt ist, wie z. B. eine eingebettete oder zitierte
      Erzählung. Für diesen Zweck wird das Element floatingText benutzt.

## Inhaltsmodell

- `<front>`
- [`<body>`](body.md)
- `<group>`
- `<back>`
- *model.global*
- *model.global*
- *model.global*
- *model.global*

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
