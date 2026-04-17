# `<addrLine>` Adresszeile

enthält eine Zeile einer Postadresse.

Adressen können entweder als eine Abfolge von Zeilen kodiert werden oder als eine beliebige Folge 
          von Elementen der model.addrPart-Klasse. Andere, nicht-postalische Formen von Adressen, 
          wie z. B. Telefonnummern oder E-Mail-Adressen, dürfen nicht direkt in ein address-Element eingeschlossen werden, 
          sondern müssen innerhalb eines addrLine-Elements kodiert werden, wenn sie Teil einer gedruckten Adresse in einer 
          Textvorlage sind.

Siehe [Textstruktur > Unterschriften](https://dokumentation.karl-barth.ch/textstruktur/unterschriften/)

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


## Content Model

```xml
<content>
    <macroRef key="macro.phraseSeq"/>
  </content>
```
