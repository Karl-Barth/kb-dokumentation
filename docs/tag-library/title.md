# `<title/>` (Titel)

**Modul:** Kernmodule

## Beschreibung

Titel mit verschiedenen Funktionen, unterschieden durch @type: Bandtitel (volume), inhaltlicher Titel (content), formaler Titel (formal), Zitierzeilen (citation_line_1–3), Editionstitel (edition) und Texttitel (text).

## Erläuterung

Die Attribute key und ref, die durch die Zugehörigkeit zur Klasse
      att.canonical verfügbar sind, können dafür verwendet werden, den
      kanonischen Titel anzugeben: Ersteres indem (z. B.) die Kennung eines Datensatzes einer externen
      Bibliothek herangezogen wird; Letzteres durch den Verweis auf ein XML-Element, das den
      kanonischen Titel enthält.

## Erlaubt in

**Header:** [`<titleStmt>`](titleStmt.md)

## Inhaltsmodell

- *macro.paraContent*

## Attribute

### `@level` (optional, geschlossene Werteliste)

gibt den bibliografischen Typ eines Titels an, d.h. ob er einen Artikel, ein Buch, eine Zeitschrift, eine Reihe oder unpubliziertes Material bezeichnet.

**Datentyp:** teidata.enumerated

**Mögliche Werte:**

- `a` — der Titel gehört zu einer unselbständigen Publikation, wie einem Artikel, Gedicht oder einem anderen Werk, das als Teil einer umfangreicheren Einheit publiziert wurde.
- `m` — der Titel bezieht sich auf Monografien wie z.B. ein Bücher oder andere selbständige Publikationen, also auch auf einzelne Bände in einem mehrbändigen Werk.
- `j` — der Titel bezieht sich auf jede Art fortlaufender oder periodischer Veröffentlichungen wie z. B. Zeitschriften, Magazine oder Zeitungen.
- `s` — der Titel bezeichnet eine Reihe von ansonsten selbständig publizierten Veröffentlichungen, wie z. B. eine Buchreihe.
- `u` — der Titel bezieht sich auf unveröffentliches Material (incl. universitäre Qualifikationsarbeiten, soweit sie nicht von einem Verlag veröffentlicht worden sind).

### `@type` (optional, geschlossene Werteliste)

klassifiziert den Titel entsprechend einer geeigneten Typologie.

**Datentyp:** teidata.enumerated

**Mögliche Werte:**

- `volume` — Bandtitel, z.B. Karl Barth - Rudolf Bultmann. Briefwechsel 1911-1966
- `content` — Inhaltlicher Titel, z.B. «Karl Barth an Rudolf Bultmann»
- `formal` — Formaler Titel (in einem Band), z.B. «Brief Nr. 4» oder «Vorwort»
- `citation_line_1` — Titel für Zitierung (erste Zeile)
- `citation_line_2` — Titel für Zitierung (zweite Zeile): Url mit Datum
- `citation_line_3` — Titel für Zitierung (dritte Zeile): Angabe des Drucks
- `edition` — Titel der Edition
- `text` — Titel (verwendet als Angabe in der aps)
- `addon` — Für Erweiterung des Titels
