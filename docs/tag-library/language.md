# `<language>` Sprache

beschreibt eine einzelne Sprache oder eine Subsprache, die innerhalb eines Textes verwendet wird.

Insbesondere für Subsprachen sollte eine Beschreibung als Inhalt des Elements angegeben werden.

**Modul:** header — Header

## Attribute

**att.global** stellt gemeinsame Attribute für alle Elemente im TEI-Kodierungsschema bereit.

**@xml:id** (optional)
:   liefert einen Identifikator für das Element, welches dieses Attribut trägt.
:   Datentyp: ID

**@n** (optional)
:   gibt eine Nummer (oder eine andere Bezeichnung) für ein Element an, die innerhalb des Dokuments nicht zwangsläufig eindeutig ist.
:   Datentyp: teidata.text

**@xml:lang** (optional)
:   gibt die Sprache des Elementinhalts durch ein Tag an, das nach BCP 47 festgelegt wird.
:   Datentyp: teidata.language

**@xml:base** (optional)
:   liefert eine Basis-URI-Referenz, mit der Anwendungen relative URI-Referenzen in absolute auflösen können.
:   Datentyp: teidata.pointer

**@xml:space** (optional, geschlossene Werteliste)
:   signalisiert die gewünschte Handhabung von Leerzeichen durch Anwendungen.
:   Datentyp: teidata.enumerated
:   `default`
:   `preserve`


**att.scope** provides attributes to describe, in general terms, the scope of an element’s application.

**@scope** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `sole`
:   `major`
:   `minor`


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
