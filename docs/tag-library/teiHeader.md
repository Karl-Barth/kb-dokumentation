# `<teiHeader/>` (TEI-Header (elektronische Titelseite))

**Modul:** Header

## Beschreibung

wird aus der Meta- und Registerdatenbank erzeugt und soll im XML nicht verändert werden (https://meta.karl-barth.ch)

## Inhaltsmodell

- [`<fileDesc>`](fileDesc.md)
- [`<revisionDesc>`](revisionDesc.md)
- *model.teiHeaderPart*

## Constraints

**header-full-citation**
:   header-full: titleStmt sollte title[@type='citation_line_1'] enthalten (Phase full).
