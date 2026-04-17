# `<teiHeader>`
*TEI-Header (elektronische Titelseite)*

wird aus der Meta- und Registerdatenbank erzeugt und soll im XML nicht verändert werden (https://meta.karl-barth.ch)

**Modul:** header

## Content-Model

`<fileDesc>`, model.teiHeaderPart, `<revisionDesc>`

## Constraints

- **header-full-citation**: header-full: titleStmt sollte title[@type='citation_line_1'] enthalten (Phase full).
