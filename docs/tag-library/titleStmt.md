# `<titleStmt>` Angaben zum Titel

sollte mehrere Titel für verschiedene Zwecke enhalten.

**Modul:** header — Header

## Enthalten in

**header:** [fileDesc](fileDesc.md) "enthält die vollständige bibliografische Beschreibung einer "

## Kann enthalten

**core:** [title](title.md) "Titel mit verschiedenen Funktionen, unterschieden durch @typ"

## Beispiele

```xml
<titleStmt>
    <title type="volume" n="vol-01">Karl Barth - Rudolf Bultmann. Briefwechsel 1911-1966</title>
    <title type="formal">Anhang Nr. 9</title>
    <title type="content">Karl Barth an Friedrich Gogarten</title>
    <title type="citation_line_1">Karl Barth an Friedrich Gogarten, 16. Juli 1928</title>
    <title type="citation_line_2">https://kbga.karl-barth.ch/texts/1119 (Stand: 21. Dezember 2020)</title>
    <title type="citation_line_3">Druck: Anhang Nr. 9, in: Karl Barth-Gesamtausgabe. Karl Barth - Rudolf Bultmann. Briefwechsel 1911-1966, Zürich 1994, S. 227–229</title>
  </titleStmt>
```

## Content Model

```xml
<content>
  <sequence minOccurs="1" maxOccurs="1">
    <elementRef key="title" minOccurs="1" maxOccurs="unbounded"/>
    <classRef key="model.respLike" minOccurs="0" maxOccurs="unbounded"/>
  </sequence>
</content>
```
