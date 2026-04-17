# `<p>` Absatz

Absatz. Darf nicht verschachtelt werden (ausser innerhalb von note).

Siehe [Textstruktur > Absatz](https://dokumentation.karl-barth.ch/textstruktur/absatz/)

[TEI Guidelines: p](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-p.html)

**Modul:** core — Kernmodule

## Attribute

**@corresp** (optional)

**@n** (optional)

**@rend** (optional)

**@xml:id** (optional)

**@xml:lang** (optional)


## Constraints

**p1**
:   p1: p darf nicht in p vorkommen (Ausnahme in note).

**abstractModel-structure-p-in-ab-or-p**
:   Abstract model violation: Paragraphs may not occur inside other paragraphs or ab elements.

**abstractModel-structure-p-in-l**
:   Abstract model violation: Metrical lines may not contain higher-level structural elements such as div, p, or ab, unless p is a child of figure or note, or is a descendant of floatingText.

## Beispiele

```xml
<p>Gottes Gebot geht mich an, sofern ich als Christ ein Glied
  seines auserwählten Volkes bin.</p>
```

## Content Model

```xml
<content>
  <macroRef key="macro.paraContent"/>
</content>
```
