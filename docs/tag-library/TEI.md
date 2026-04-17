# `<TEI/>` (TEI-Dokument)

**Modul:** Textstruktur

## Beschreibung

enthält ein einzelnes TEI-konformes Dokument, das aus einem einzigen TEI-Header und einem oder
    mehreren Mitgliedern der model.resource-Klasse besteht. Mehrere
    TEI-Elemente können in einem teiCorpus-Element zusammengefasst werden.

## Erläuterung

Dieses Element ist obligatorisch. Es ist notwendig, 
      auch den TEI-Namensraum http://www.tei-c.org/ns/1.0 anzugeben, z.B. 
      TEI version="4.4.0" xml:lang="it" 
        xmlns="http://www.tei-c.org/ns/1.0".

## Erlaubt in

**Textstruktur:** [`<TEI>`](TEI.md)

## Inhaltsmodell

- [`<teiHeader>`](teiHeader.md)
- [`<TEI>`](TEI.md)
- [`<TEI>`](TEI.md)
- *model.resource*

## Attribute

### `@version` (optional)

gibt die Versionsnummer der TEI-Richtlinien an, gegen die dieses Dokument validiert wird.

**Datentyp:** teidata.version
