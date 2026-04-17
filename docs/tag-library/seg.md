# `<seg>` arbiträres Segment

Segment. Verwendet für nicht-Entitäten, Verse, Biogramme, Hervorhebungen und Übersetzungen.

Das seg-Element kann nach Gutdünken verwendet werden, um jegliches Textsegment, welches
      für eine Weiterverarbeitung relevant sein könnte, auszuzeichnen. Eine Anwendung des Elements ist
      die Auszeichnung von Textmerkmalen, für welche sonst kein dediziertes Markup verfügbar ist. Ein
      anderer Anwendungsfall ist, einen Identifikator für ein Textsegment anzubieten, um von anderen
      Elementen auf dieses Segment verweisen zu können, z. B. um ein Ziel für einen ptr oder
      ein ähnliches Element zur Verfügung zu stellen.

**Modul:** linking — Linking

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


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


**att.segLike** provides attributes for elements used for arbitrary segmentation.

**@function** (optional)
:   Datentyp: teidata.enumerated


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


## Content Model

```xml
<content>
  <macroRef key="macro.paraContent"/>
</content>
```
