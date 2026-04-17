# `<language/>` (Sprache)

**Modul:** Header

## Beschreibung

beschreibt eine einzelne Sprache oder eine Subsprache, die innerhalb eines Textes verwendet wird.

## Inhaltsmodell

- *macro.phraseSeq.limited*

## Attribute

### `@ident`

gibt einen Sprachcode, aufgebaut nach BCP 47 an, 
            der zur Identifikation der im Element dokumentierten Sprache benutzt wird und auf den das globale xml:lang-Attribut verweist.

**Datentyp:** `teidata.language`

### `@usage`

gibt den ungefähren prozentualen Anteil des Textes an, der in dieser Sprache verfasst wurde.

**Datentyp:** `nonNegativeInteger`
