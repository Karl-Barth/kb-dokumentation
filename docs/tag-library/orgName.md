# `<orgName>`

Name einer Organisation mit Verweis auf die Meta-DB via @ref.

Siehe [Textelemente > Akteure](https://dokumentation.karl-barth.ch/textelemente/akteure/)

**Modul:** namesdates — Namen und Daten

## Attribute

**att.canonical** provides attributes that can be used to associate a representation such as a name or title
    with canonical information about the object being named or referenced.

**@key** (optional)
:   Datentyp: teidata.text

**@ref** (optional)
:   Datentyp: teidata.pointer


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


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


## Beispiele

```xml
<orgName ref="kbga-actors-8209">Theologische Fakultät Göttingen</orgName>
```

## Content Model

```xml
<content>
  <macroRef key="macro.phraseSeq"/>
</content>
```
