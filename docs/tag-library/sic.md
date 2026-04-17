# `<sic>` Lateinisch für 'auf diese Weise', 'so'

Markiert die fehlerhafte Stelle in der Druckausgabe (innerhalb von choice/sic/corr). Das @ed gibt die Ausgabe an (typisch: pga).

Siehe [Textelemente > Korrektionen Der Druckausgabe](https://dokumentation.karl-barth.ch/textelemente/korrektionen-der-druckausgabe/)

[TEI Guidelines: sic](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-sic.html)

**Modul:** core — Kernmodule

## Attribute

**@ed** (optional)


## Beispiele

**Beispiel 1:**

```xml
I don't know, Juan. It's so far in the past now
      — how
<sic>we can</sic> prove or disprove anyone's theories?
```

**Beispiel 2:**

```xml
I don't know, Juan. It's so far in the past now
      — how
<choice>
  <sic>we can</sic>
  <corr>can we</corr>
</choice> prove or disprove anyone's theories?
```

## Content Model

```xml
<content>
  <macroRef key="macro.paraContent"/>
</content>
```
