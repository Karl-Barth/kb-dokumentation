# `<foreign/>` (fremd)

**Modul:** Kernmodule

## Beschreibung

identifiziert ein Wort oder eine Phrase, die zu einer anderen Sprache gehört, als der umgebende Text.

## Erläuterung

Das globale xml:lang-Attribut sollte mit diesem Element verwendet werden, um die
      Sprache des markierten Wortes oder der markierten Phrase anzugeben. Der Wert dieses Attributs
      soll den Empfehlungen von 6.1. Language Identification folgen.
    Das foreign-Element sollte nur dann benutzt werden, wenn sonst keine anderen
      Elemente zur Verfügung stehen, um das betroffene Wort oder die Phrase zu markieren. Wird das
        foreign-Element nicht verwendet, sollte das globale xml:lang-Attribut
      bevorzugt verwendet werden, um eine Sprache dem Inhalt eines Elements zuzuweisen.
    Das distinct-Element kann verwendet werden, um Phrasen, die zu Subsprachen,
      Sprachregister oder Varietäten gehören, auszuzeichnen.

Ausführliche Dokumentation:

- [Textelemente > Fremdsprache](https://dokumentation.karl-barth.ch/textelemente/fremdsprache/)

## Inhaltsmodell

- *macro.phraseSeq*
