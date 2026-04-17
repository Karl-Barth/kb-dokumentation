# `<bibl/>` (bibliografische Angabe)

**Modul:** Kernmodule

## Beschreibung

Bibliographische Angabe. Unterscheidet zwischen gedruckter Gesamtausgabe (pga), Alexander Street Press (asp), Quellen (source) und Liedern (song).

## Erläuterung

Ausführliche Dokumentation:

- [Textelemente > Literatur](https://dokumentation.karl-barth.ch/textelemente/literatur/)

## Inhaltsmodell

- Beliebiger Textinhalt
- *model.gLike*
- *model.highlighted*
- *model.pPart.data*
- *model.pPart.edit*
- *model.segLike*
- *model.ptrLike*
- *model.biblPart*
- *model.global*

## Attribute

### `@type` (optional)

**Mögliche Werte:**

- `pga` — Printed Gesamtausgabe (Ausgabe des TVZ)
- `asp` — Alexander Street Press (digital edition)
- `source` — Quelle für einen Text der KBGA

### `@subtype` (optional, geschlossene Werteliste)

Angabe der Funktion einer Quelle für den edierten Text

**Mögliche Werte:**

- `Vorlage_der_Edition`
- `Weitere_Vorlage`
- `Material_zum_Kontext`
- `rkg` — Gesangsbuch der evangelisch-reformierten Kirchen der deutschsprachigen Schweiz (1952)
- `ekg` — Deutsches Evangelisches Kirchengesangbuch (1950)
- `erkg` — Gesangbuch für die evangelisch-reformirte Kirche der deutschen Schweiz (1891)
- `eg` — Evangelisches Gesangsbuch Deutschlands (1993ff.)
- `rg` — Reformiertes Gesangsbuch der deutschsprachigen Schweiz (1998)
- `reichslieder` — Reichs-Lieder. Deutsches Gemeinschafts-Liederbuch

### `@n` (optional)

Bezeichnung der Quelle für einen edierten Text

**Datentyp:** string — Pattern: `[A-Z][0-9]?`

### `@xml:id` (optional)

**Datentyp:** ID — Pattern: `(b[\-0-9]+|pga|asp|kbga-(sources|bibls|songs|actors|places|keywords)-[0-9]+|[A-Z]\d*)`

## Constraints

**song1**
:   song1: bibl[@type='song'] muss @corresp enthalten.

**song2**
:   song2: bibl[@type='song'] darf keinen @subtype enthalten.

## Beispiele

```xml
<bibl xml:id="A" type="source">A (Vorlage der Edition): Bultmann, Rudolf, Rudolf Bultmann an Karl Barth, 11. Juni 1911. <ref target="https://kba.karl-barth.ch/objects/7950">KBA 9311.73</ref>.</bibl>
```
