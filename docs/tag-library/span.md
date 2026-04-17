# `<span>`

associates an interpretative annotation directly with a span of text.

**Modul:** analysis

## Attribute

| Attribut | Beschreibung | Werte |
|----------|-------------|-------|
| `@from` |  | teidata.pointer |
| `@to` |  | teidata.pointer |

## Content-Model

macro.phraseSeq.limited

## Constraints

- **target-from**: Only one of the attributes @target and @from may be supplied on
- **targetto**: Only one of the attributes @target and @to may be supplied on
- **tonotfrom**: If @to is supplied on , @from must be supplied as well
- **tofrom**: The attributes @to and @from on  may each contain only a single value
