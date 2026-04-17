# `<addrLine>` Adresszeile

enthält eine Zeile einer Postadresse.

Adressen können entweder als eine Abfolge von Zeilen kodiert werden oder als eine beliebige Folge 
          von Elementen der model.addrPart-Klasse. Andere, nicht-postalische Formen von Adressen, 
          wie z. B. Telefonnummern oder E-Mail-Adressen, dürfen nicht direkt in ein address-Element eingeschlossen werden, 
          sondern müssen innerhalb eines addrLine-Elements kodiert werden, wenn sie Teil einer gedruckten Adresse in einer 
          Textvorlage sind.

Siehe [Textstruktur > Unterschriften](https://dokumentation.karl-barth.ch/textstruktur/unterschriften/)

[TEI Guidelines: addrLine](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-addrLine.html)

**Modul:** core — Kernmodule

## Attribute

**@rendition** (optional)


## Content Model

```xml
<content>
    <macroRef key="macro.phraseSeq"/>
  </content>
```
