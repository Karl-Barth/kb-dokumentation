# `<term>` Fachbegriff

enthält ein einzelnes Wort, Mehrworttermini 
        oder symbolische Bezeichnungen, die als Fachbegriffe verstanden werden.

Wenn dieses Element innerhalb eines index-Elements auftritt, so wird es als Lemma dieses 
          Index-Eintrags angesehen. An anderer Stelle wird es einfach als Auszeichnung eines Fachbegriffs gewertet.
          Das term-Element kann mit einem entsprechenden gloss-Element über sein ref-Attribut 
          verknüpft werden; alternativ kann die Verknüpfung auch über das target-Attribut am gloss-Element 
          hergestellt werden.
      
      
          Es wird keine Position im Theoriediskurs bezogen, ob Fachbegriffe atomare oder größere lexikalische Einheiten umfassen können; 
          das term-Element kann für jedwede dieser Einheiten eingesetzt werden. Weiterhin wird keine Definition von "Fachbegriff" 
          gegeben, sondern jeder praktische Einsatz sanktioniert.
      
      
          So wie auch andere Mitglieder der Attributklasse att.canonical können term-Elemente im 
          laufenden Text mit entsprechenden kanonischen Definitionen verknüpft werden; entweder mittels einer URI (über das 
          ref-Attribut) oder mittels eines speziellen Codes (über das key-Attribut).
          Da sich die Attribute target und cRef gegenseitig ausschließen und mit dem ref-Attribut überlappen, 
          sind diese als "veraltet" gekennzeichnet und können mit einer der folgenden Guideline-Auflagen entfernt werden.

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


**att.canonical** provides attributes that can be used to associate a representation such as a name or title
    with canonical information about the object being named or referenced.

**@key** (optional)
:   Datentyp: teidata.text

**@ref** (optional)
:   Datentyp: teidata.pointer


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


**att.declaring** provides attributes for elements which may be independently associated with a particular declarable element within the header, thus overriding the inherited default for that element.

**@decls** (optional)
:   Datentyp: teidata.pointer


**att.pointing** provides a set of attributes used by all elements which point
  to other elements by means of one or more URI references.

**@target** (optional)
:   Datentyp: teidata.pointer


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


## Enthalten in

**header:** [keywords](keywords.md) "enthält eine Zusammenstellung von Schlagwörtern oder Phrasen"

## Content Model

```xml
<content>
    <macroRef key="macro.phraseSeq"/>
  </content>
```
