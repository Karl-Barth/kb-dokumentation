# `<abbr>` Abkürzung

Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref.

Werden Abkürzungen stillschweigend aufgelöst, 
    sollte diese Vorgehensweise im TEI-Header über das editorialDecl-Element dokumentiert werden, 
    entweder in einem normalization- oder einem p-Element.

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


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


**@type** (optional)
:   erlaubt es, die Abkürzung nach einer geeigneten Typologie zu klassifizieren.
:   Datentyp: teidata.enumerated
:   `suspension` — die Abkürzung gibt nur den Anfang des Wortes oder der Phrase, der Rest wird weggelassen, z. B. H(ansestadt) H(amburg), u(nd) s(o) w(eiter).
:   `contraction` — die Abkürzung lässt Buchstaben im Wortinneren weg.
:   `brevigraph` — die Abkürzung verwendet ein spezielles Zeichen für die ausgelassenen Buchstaben.
:   `superscription` — die Abkürzung enthält Zeichen auf oder über der Mittellinie.
:   `acronym` — die Abkürzung besteht aus den Anfangsbuchstaben mehrer Wörter.
:   `title` — eine Abkürzung für eine Anrede oder einen akademischen Titel (Dr., Hr., Fr., ...)
:   `organization` — eine Abkürzung für den Namen einer Organisation.
:   `geographic` — die Abkürzung steht für einen geografischen Namen.


## Beispiele

```xml
<abbr type="acron">CVJM</abbr>
```

## Content Model

```xml
<content>
  <macroRef key="macro.phraseSeq"/>
</content>
```
