# `<language/>` (Sprache)

**Modul:** Header

## Beschreibung

beschreibt eine einzelne Sprache oder eine Subsprache, die innerhalb eines Textes verwendet wird.

## Erläuterung

Insbesondere für Subsprachen sollte eine Beschreibung als Inhalt des Elements angegeben werden.

## Erlaubt in

**Header:** [`<langUsage>`](langUsage.md)

## Inhaltsmodell

- *macro.phraseSeq.limited*

## Attribute

### `@ident` (erforderlich)

gibt einen Sprachcode, aufgebaut nach BCP 47 an, 
            der zur Identifikation der im Element dokumentierten Sprache benutzt wird und auf den das globale xml:lang-Attribut verweist.

**Datentyp:** teidata.language

### `@usage` (optional)

gibt den ungefähren prozentualen Anteil des Textes an, der in dieser Sprache verfasst wurde.

**Datentyp:** nonNegativeInteger
