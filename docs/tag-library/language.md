# `<language>` Sprache

beschreibt eine einzelne Sprache oder eine Subsprache, die innerhalb eines Textes verwendet wird.

Insbesondere für Subsprachen sollte eine Beschreibung als Inhalt des Elements angegeben werden.

**Modul:** header — Header

## Attribute

**@ident** (erforderlich)
:   gibt einen Sprachcode, aufgebaut nach BCP 47 an, 
            der zur Identifikation der im Element dokumentierten Sprache benutzt wird und auf den das globale xml:lang-Attribut verweist.
:   Datentyp: teidata.language

**@usage** (optional)
:   gibt den ungefähren prozentualen Anteil des Textes an, der in dieser Sprache verfasst wurde.
:   Datentyp: nonNegativeInteger


## Enthalten in

**header:** [langUsage](langUsage.md) "beschreibt Sprachen, Subsprachen, Register, Dialekte usw., d"

## Content Model

```xml
<content>
    <macroRef key="macro.phraseSeq.limited"/>
  </content>
```
