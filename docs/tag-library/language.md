# `<language>`
*Sprache*

beschreibt eine einzelne Sprache oder eine Subsprache, die innerhalb eines Textes verwendet wird.

**Modul:** header

## Attribute

| Attribut | Beschreibung | Werte |
|----------|-------------|-------|
| `@ident` | gibt einen Sprachcode, aufgebaut nach BCP 47 an, 
            der zur Identifikation der im Element dokumentierten Sprache benutzt wird und auf den das globale xml:lang-Attribut verweist. | teidata.language |
| `@usage` | gibt den ungefähren prozentualen Anteil des Textes an, der in dieser Sprache verfasst wurde. | nonNegativeInteger |

## Content-Model

macro.phraseSeq.limited
