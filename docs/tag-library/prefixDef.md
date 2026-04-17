# `<prefixDef>`

defines a prefixing scheme used in teidata.pointer values,
  showing how abbreviated URIs using the scheme may be expanded into full URIs.

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


**att.patternReplacement** provides attributes for regular-expression matching and replacement.

**@matchPattern** (erforderlich)
:   Datentyp: teidata.pattern

**@replacementPattern** (erforderlich)
:   beschreibt ein replacement pattern
        (Ersetzungsmuster), das heißt das Grundgerüst einer relativen oder absoluten URI, die Referenzen auf Gruppen im matchPattern-Attribut enthalten und die URI komplettieren, sobald die  
        Ersetzung der untergeordneten Muster durchgeführt wurde.
:   Datentyp: teidata.replacement


**@ident** (erforderlich)
:   Datentyp: teidata.prefix


## Enthalten in

**header:** [listPrefixDef](listPrefixDef.md) "contains a list of definitions of prefixing schemes used in "

## Content Model

```xml
<content>
      <classRef key="model.pLike" minOccurs="0" maxOccurs="unbounded"/>
  </content>
```
