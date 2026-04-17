# `<TEI>`
*TEI-Dokument*

enthält ein einzelnes TEI-konformes Dokument, das aus einem einzigen TEI-Header und einem oder
    mehreren Mitgliedern der model.resource-Klasse besteht. Mehrere
    TEI-Elemente können in einem teiCorpus-Element zusammengefasst werden.

**Modul:** textstructure

## Attribute

| Attribut | Beschreibung | Werte |
|----------|-------------|-------|
| `@version` | gibt die Versionsnummer der TEI-Richtlinien an, gegen die dieses Dokument validiert wird. | teidata.version |

## Content-Model

`<teiHeader>`, model.resource, `<TEI>`, `<TEI>`
