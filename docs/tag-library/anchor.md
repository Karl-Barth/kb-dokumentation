# `<anchor>` Ankerpunkt

Ankerpunkt für Querverweise (@type='cross') und für Fussnoten mit mehreren Fussnotenzeichen (@type='note').

Siehe [Textstruktur > Anmerkungen](https://dokumentation.karl-barth.ch/textstruktur/anmerkungen/)
Siehe [Textelemente > Querverweise](https://dokumentation.karl-barth.ch/textelemente/querverweise/)

[TEI Guidelines: anchor](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-anchor.html)

**Modul:** linking — Linking

## Attribute

**@type** (optional, geschlossene Werteliste)
:   Wird für Querverweise und für Fussnoten verwendet, die im Text mehrere Fussnotenzeichen haben.
:   `cross` — Anker für Querverweis
:   `note` — Stelle für zweites Fussnotenzeichen; in der note/@target wird die @xml:id gesetzt

**@n** (optional)

**@xml:id** (optional)


## Kann enthalten

Leeres Element.

## Beispiele

```xml
<anchor n="1" xml:id="n1511a"/>
```

## Content Model

```xml
<content>
  <empty/>
</content>
```
