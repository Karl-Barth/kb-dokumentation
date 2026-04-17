# `<cell>` Tabellenzelle

Tabellenzelle.

Siehe [Textstruktur > Tabellen](https://dokumentation.karl-barth.ch/textstruktur/tabellen/)

**Modul:** figures — Abbildungen und Tabellen

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


**att.tableDecoration** provides attributes used to decorate rows or cells of a table.

**@role** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `label`
:   `data`

**@rows** (optional)
:   Datentyp: teidata.count

**@cols** (optional)
:   Datentyp: teidata.count


## Enthalten in

**figures:** [row](row.md) "enthält eine Zeile einer Tabelle."

## Content Model

```xml
<content>
  <macroRef key="macro.specialPara"/>
</content>
```
