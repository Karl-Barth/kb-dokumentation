# `<msIdentifier/>`

**Modul:** Handschriftenbeschreibung

## Beschreibung

contains the information required to identify the manuscript or similar object being described.

## Erlaubt in

**Handschriftenbeschreibung:** [`<msDesc>`](msDesc.md)

## Inhaltsmodell

- `<institution>`
- [`<repository>`](repository.md)
- `<collection>`
- [`<idno>`](idno.md)
- `<msName>`
- `<objectName>`
- [`<altIdentifier>`](altIdentifier.md)
- *model.placeNamePart*

## Constraints

**msId_minimal**
:   An msIdentifier must contain either a repository or location.
