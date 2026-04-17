# `<rs/>` (verweisende Zeichenkette)

**Modul:** Kernmodule

## Beschreibung

Referenzierende Zeichenkette für Akteure, die nicht als persName oder orgName ausgezeichnet werden (z.B. Pronomen, Umschreibungen). Der @type unterscheidet person, organisation, place, conference.

## Erläuterung

Ausführliche Dokumentation:

- [Textelemente > Akteure](https://dokumentation.karl-barth.ch/textelemente/akteure/)

## Inhaltsmodell

- *macro.phraseSeq*

## Attribute

### `@type` (optional)

**Mögliche Werte:**

- `conference`
- `person`
- `organisation`
- `place`

## Beispiele

```xml
<rs type="person" ref="kbga-actors-27">Bruders</rs>
```
