# `<choice/>` (Alternative)

**Modul:** Kernmodule

## Beschreibung

Gruppiert sic/corr-Paare für Korrekturen der Druckausgabe.

## Erläuterung

Ausführliche Dokumentation:

- [Textelemente > Korrektionen Der Druckausgabe](https://dokumentation.karl-barth.ch/textelemente/korrektionen-der-druckausgabe/)

## Erlaubt in

**Kernmodule:** [`<choice>`](choice.md)

## Inhaltsmodell

- [`<choice>`](choice.md)
- *model.choicePart*

## Beispiele

```xml
<choice>
                <sic source="pga">Ernst</sic>
                <corr resp="ak" type="corr">Emil</corr>
              </choice> Balla
```
