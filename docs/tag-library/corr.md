# `<corr>` Korrektur

Korrektur eines Fehlers in der Druckausgabe. Der @type unterscheidet inhaltliche Korrekturen (corr), Druckfehler (misprint) und veraltete Angaben (update).

Siehe [Textelemente > Korrektionen Der Druckausgabe](https://dokumentation.karl-barth.ch/textelemente/korrektionen-der-druckausgabe/)

[TEI Guidelines: corr](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-corr.html)

**Modul:** core — Kernmodule

## Attribute

**@type** (optional, geschlossene Werteliste)
:   `corr` — korrigiert einen inhaltlichen Fehler
:   `misprint` — korrigiert einen Druckfehler
:   `update` — wenn Angaben veraltet sind, z.B. URLs

**@resp** (optional)


## Beispiele

```xml
<choice>
    <sic source="pga">Ernst</sic>
    <corr resp="ak" type="corr">Emil</corr>
  </choice> Balla
```

## Content Model

```xml
<content>
  <macroRef key="macro.paraContent"/>
</content>
```
