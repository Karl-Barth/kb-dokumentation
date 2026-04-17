# `<span/>`

**Modul:** Analyse

## Beschreibung

associates an interpretative annotation directly with a span of text.

## Inhaltsmodell

- *macro.phraseSeq.limited*

## Attribute

### `@from` (optional)

**Datentyp:** teidata.pointer

### `@to` (optional)

**Datentyp:** teidata.pointer

## Constraints

**target-from**
:   Only one of the attributes @target and @from may be supplied on

**targetto**
:   Only one of the attributes @target and @to may be supplied on

**tonotfrom**
:   If @to is supplied on , @from must be supplied as well

**tofrom**
:   The attributes @to and @from on  may each contain only a single value
