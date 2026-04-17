# `<foreign>` fremd

identifiziert ein Wort oder eine Phrase, die zu einer anderen Sprache gehört, als der umgebende Text.

Das globale xml:lang-Attribut sollte mit diesem Element verwendet werden, um die
      Sprache des markierten Wortes oder der markierten Phrase anzugeben. Der Wert dieses Attributs
      soll den Empfehlungen von 6.1. Language Identification folgen.
    Das foreign-Element sollte nur dann benutzt werden, wenn sonst keine anderen
      Elemente zur Verfügung stehen, um das betroffene Wort oder die Phrase zu markieren. Wird das
        foreign-Element nicht verwendet, sollte das globale xml:lang-Attribut
      bevorzugt verwendet werden, um eine Sprache dem Inhalt eines Elements zuzuweisen.
    Das distinct-Element kann verwendet werden, um Phrasen, die zu Subsprachen,
      Sprachregister oder Varietäten gehören, auszuzeichnen.

Siehe [Textelemente > Fremdsprache](https://dokumentation.karl-barth.ch/textelemente/fremdsprache/)

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


## Content Model

```xml
<content>
    <macroRef key="macro.phraseSeq"/>
  </content>
```
