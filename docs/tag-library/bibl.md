# `<bibl>`
*bibliografische Angabe*

Bibliographische Angabe. Unterscheidet zwischen gedruckter Gesamtausgabe (pga), Alexander Street Press (asp), Quellen (source) und Liedern (song).

!!! note "Dokumentation"
    - [Literatur](https://dokumentation.karl-barth.ch/textelemente/literatur/)

**Modul:** core

## Attribute

| Attribut | Beschreibung | Werte |
|----------|-------------|-------|
| `@type` |  | `pga`, `asp`, `source` |
| `@subtype` | Angabe der Funktion einer Quelle für den edierten Text | `Vorlage_der_Edition`, `Weitere_Vorlage`, `Material_zum_Kontext`, `rkg`, `ekg`, `erkg`, `eg`, `rg`, `reichslieder` (geschlossen) |
| `@n` | Bezeichnung der Quelle für einen edierten Text | string ([A-Z][0-9]?) |
| `@xml:id` |  | ID ((b[\-0-9]+|pga|asp|kbga-(sources|bibls|songs|actors|places|keywords)-[0-9]+|[A-Z]\d*)) |

### `@type`

- **`pga`**: Printed Gesamtausgabe (Ausgabe des TVZ)
- **`asp`**: Alexander Street Press (digital edition)
- **`source`**: Quelle für einen Text der KBGA

### `@subtype`

- **`rkg`**: Gesangsbuch der evangelisch-reformierten Kirchen der deutschsprachigen Schweiz (1952)
- **`ekg`**: Deutsches Evangelisches Kirchengesangbuch (1950)
- **`erkg`**: Gesangbuch für die evangelisch-reformirte Kirche der deutschen Schweiz (1891)
- **`eg`**: Evangelisches Gesangsbuch Deutschlands (1993ff.)
- **`rg`**: Reformiertes Gesangsbuch der deutschsprachigen Schweiz (1998)
- **`reichslieder`**: Reichs-Lieder. Deutsches Gemeinschafts-Liederbuch

## Content-Model

Text, model.gLike, model.highlighted, model.pPart.data, model.pPart.edit, model.segLike, model.ptrLike, model.biblPart, model.global

## Constraints

- **song1**: song1: bibl[@type='song'] muss @corresp enthalten.
- **song2**: song2: bibl[@type='song'] darf keinen @subtype enthalten.
