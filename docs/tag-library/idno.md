# `<idno/>` (Identifikator)

**Modul:** Header

## Beschreibung

Identifikator, z.B. URL oder KBA-Objektnummer.

## Erläuterung

Ausführliche Dokumentation:

- [Textelemente > Querverweise](https://dokumentation.karl-barth.ch/textelemente/querverweise/)

## Erlaubt in

**Header:** [`<idno>`](idno.md)

**Namen und Daten:** [`<event>`](event.md)

**Handschriftenbeschreibung:** [`<altIdentifier>`](altIdentifier.md), [`<msIdentifier>`](msIdentifier.md)

## Inhaltsmodell

- Beliebiger Textinhalt
- [`<idno>`](idno.md)
- *model.gLike*

## Attribute

### `@xml:id` (optional)

### `@type` (optional, erweiterbare Werteliste)

bestimmt die Art des Identifikators (z. B. ISBN, Sozialversicherungsnummer, URI)

**Datentyp:** teidata.enumerated

**Mögliche Werte:**

- `ISBN`
- `ISSN`
- `DOI`
- `URI`
- `VIAF`
- `ESTC`
- `OCLC`

## Beispiele

```xml
<idno type="ISBN">978-1-906964-22-1</idno>
<idno type="ISSN">0143-3385</idno>
<idno type="DOI">10.1000/123</idno>
<idno type="URI">http://www.worldcat.org/oclc/185922478</idno>
<idno type="URI">http://authority.nzetc.org/463/</idno>
<idno type="LT">Thomason Tract E.537(17)</idno>
<idno type="Wing">C695</idno>
<idno type="oldCat"><g ref="#sym"/>345</idno>
```
