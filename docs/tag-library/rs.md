# `<rs>` verweisende Zeichenkette

Referenzierende Zeichenkette für Akteure, die nicht als persName oder orgName ausgezeichnet werden (z.B. Pronomen, Umschreibungen). Der @type unterscheidet person, organisation, place, conference.

Siehe [Textelemente > Akteure](https://dokumentation.karl-barth.ch/textelemente/akteure/)

[TEI Guidelines: rs](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-rs.html)

**Modul:** core — Kernmodule

## Attribute

**@type** (optional)
:   `conference`
:   `person`
:   `organisation`
:   `place`

**@n** (optional)

**@ref** (optional)


## Beispiele

```xml
<rs type="person" ref="kbga-actors-27">Bruders</rs>
```

## Content Model

```xml
<content>
  <macroRef key="macro.phraseSeq"/>
</content>
```
