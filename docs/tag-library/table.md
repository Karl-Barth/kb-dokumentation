# `<table/>` (Tabelle)

**Modul:** Abbildungen und Tabellen

## Beschreibung

enthält Text, der in Tabellenform, also in Zeilen und Spalten, dargestellt ist.

## Erläuterung

Enthält eine Reihe von Zeilen und optional eine Überschrift.
    Jegliche Information die grafische Darstellung betreffend, sollte mit dem globalen
      rend-Attribut auf der Ebene von Tabelle, Zeile oder Zelle verzeichnet werden.

Ausführliche Dokumentation:

- [Textstruktur > Tabellen](https://dokumentation.karl-barth.ch/textstruktur/tabellen/)

## Inhaltsmodell

- [`<row>`](row.md)
- *model.headLike*
- *model.global*
- *model.global*
- *model.graphicLike*
- *model.global*
- *model.divBottom*
- *model.global*

## Attribute

### `@rows` (optional)

gibt die Anzahl der Tabellenzeilen an.

**Datentyp:** teidata.count

### `@cols` (optional)

gibt die Anzahl der Tabellenspalten an.

**Datentyp:** teidata.count
