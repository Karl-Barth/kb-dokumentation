# `<table>` Tabelle

Tabelle.

Siehe [Textstruktur > Tabellen](https://dokumentation.karl-barth.ch/textstruktur/tabellen/)

**Modul:** figures — Abbildungen und Tabellen

## Attribute

**@rows** (optional)
:   gibt die Anzahl der Tabellenzeilen an.
:   Datentyp: teidata.count

**@cols** (optional)
:   gibt die Anzahl der Tabellenspalten an.
:   Datentyp: teidata.count


## Kann enthalten

**figures:** [row](row.md) "enthält eine Zeile einer Tabelle."

## Content Model

```xml
<content>
  <sequence minOccurs="1" maxOccurs="1">
    <alternate minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.headLike"/>
      <classRef key="model.global"/>
    </alternate>
    <alternate minOccurs="1" maxOccurs="1">
      <sequence minOccurs="1" maxOccurs="unbounded">
        <elementRef key="row"/>
        <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
      </sequence>
      <sequence minOccurs="1" maxOccurs="unbounded">
        <classRef key="model.graphicLike"/>
        <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
      </sequence>
    </alternate>
    <sequence minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.divBottom"/>
      <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
    </sequence>
  </sequence>
</content>
```
