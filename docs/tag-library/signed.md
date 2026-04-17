# `<signed>` Signatur

enthält die abschließende Grußformel o.Ä. die ein Vorwort, eine Widmung oder einen anderen Abschnitt des Textes beendet.

Siehe [Textstruktur > Unterschriften](https://dokumentation.karl-barth.ch/textstruktur/unterschriften/)

[TEI Guidelines: signed](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-signed.html)

**Modul:** textstructure — Textstruktur

## Attribute

**@rend** (optional)

**@rendition** (optional)


## Enthalten in

**textstructure:** [closer](closer.md) "Schlussformel eines Briefes (Gruss, Unterschrift, Datum)." [opener](opener.md) "fasst Datumszeile, Verfasserangabe, Anredeformel und ähnlich"

## Content Model

```xml
<content>
    <macroRef key="macro.paraContent"/>
  </content>
```
