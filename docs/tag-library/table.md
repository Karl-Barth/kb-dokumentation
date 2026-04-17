# `<table>`
*Tabelle*

enthält Text, der in Tabellenform, also in Zeilen und Spalten, dargestellt ist.

!!! note "Dokumentation"
    - [Tabellen](https://dokumentation.karl-barth.ch/textstruktur/tabellen/)

**Modul:** figures

## Attribute

| Attribut | Beschreibung | Werte |
|----------|-------------|-------|
| `@rows` | gibt die Anzahl der Tabellenzeilen an. | teidata.count |
| `@cols` | gibt die Anzahl der Tabellenspalten an. | teidata.count |

## Content-Model

model.headLike, model.global, `<row>`, model.global, model.graphicLike, model.global, model.divBottom, model.global
