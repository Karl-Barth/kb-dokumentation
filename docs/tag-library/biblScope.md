# `<biblScope>` Geltungsbereich einer bibliografischen Referenz

Umfangsangabe innerhalb einer bibliographischen Referenz (Seiten, Teilnummer).

**Modul:** core — Kernmodule

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


**att.citing** provides attributes for specifying the specific part of a bibliographic item being cited.

**@unit** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `volume`
:   `issue`
:   `page`
:   `line`
:   `chapter`
:   `part`
:   `column`
:   `entry`

**@from** (optional)
:   Datentyp: teidata.word

**@to** (optional)
:   Datentyp: teidata.word


**@unit** (optional, geschlossene Werteliste)


## Content Model

```xml
<content>
  <macroRef key="macro.phraseSeq"/>
</content>
```
