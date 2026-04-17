# `<seg>` arbiträres Segment

Segment. Verwendet für nicht-Entitäten, Verse, Biogramme, Hervorhebungen und Übersetzungen.

Das seg-Element kann nach Gutdünken verwendet werden, um jegliches Textsegment, welches
      für eine Weiterverarbeitung relevant sein könnte, auszuzeichnen. Eine Anwendung des Elements ist
      die Auszeichnung von Textmerkmalen, für welche sonst kein dediziertes Markup verfügbar ist. Ein
      anderer Anwendungsfall ist, einen Identifikator für ein Textsegment anzubieten, um von anderen
      Elementen auf dieses Segment verweisen zu können, z. B. um ein Ziel für einen ptr oder
      ein ähnliches Element zur Verfügung zu stellen.

[TEI Guidelines: seg](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-seg.html)

**Modul:** linking — Linking

## Attribute

**@corresp** (optional)

**@n** (optional)

**@type** (optional)

**@xml:id** (optional)

**@xml:lang** (optional)


## Content Model

```xml
<content>
  <macroRef key="macro.paraContent"/>
</content>
```
