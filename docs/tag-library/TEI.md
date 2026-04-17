# `<TEI>` TEI-Dokument

enthält ein einzelnes TEI-konformes Dokument, das aus einem einzigen TEI-Header und einem oder
    mehreren Mitgliedern der model.resource-Klasse besteht. Mehrere
    TEI-Elemente können in einem teiCorpus-Element zusammengefasst werden.

Dieses Element ist obligatorisch. Es ist notwendig, 
      auch den TEI-Namensraum http://www.tei-c.org/ns/1.0 anzugeben, z.B. 
      TEI version="4.4.0" xml:lang="it" 
        xmlns="http://www.tei-c.org/ns/1.0".

**Modul:** textstructure — Textstruktur

## Attribute

**@version** (optional)
:   gibt die Versionsnummer der TEI-Richtlinien an, gegen die dieses Dokument validiert wird.
:   Datentyp: teidata.version


## Enthalten in

**textstructure:** [TEI](TEI.md) "enthält ein einzelnes TEI-konformes Dokument, das aus einem "

## Kann enthalten

**textstructure:** [TEI](TEI.md) "enthält ein einzelnes TEI-konformes Dokument, das aus einem "

**header:** [teiHeader](teiHeader.md) "wird aus der Meta- und Registerdatenbank erzeugt und soll im"

## Content Model

```xml
<content>
    
    <sequence>
      <elementRef key="teiHeader"/>
      <alternate>
        <sequence>
          <classRef key="model.resource" minOccurs="1" maxOccurs="unbounded"/>
          <elementRef key="TEI" minOccurs="0" maxOccurs="unbounded"/>
        </sequence>
        <elementRef key="TEI" minOccurs="1" maxOccurs="unbounded"/>
      </alternate>
    </sequence>
  </content>
```
