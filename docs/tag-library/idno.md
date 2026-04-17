# `<idno/>` (Identifikator)

**Modul:** Header

## Beschreibung

Identifikator, z.B. URL oder KBA-Objektnummer.

!!! note "Ausführliche Dokumentation"
    [Textelemente > Querverweise](https://dokumentation.karl-barth.ch/textelemente/querverweise/)


## Inhaltsmodell

- Beliebiger Textinhalt
- [`<idno>`](idno.md)
- *model.gLike*

## Attribute

### `@xml:id`

### `@type` (erweiterbare Werteliste)

bestimmt die Art des Identifikators (z. B. ISBN, Sozialversicherungsnummer, URI)

**Datentyp:** `teidata.enumerated`

**Mögliche Werte:**

- `ISBN`
- `ISSN`
- `DOI`
- `URI`
- `VIAF`
- `ESTC`
- `OCLC`
