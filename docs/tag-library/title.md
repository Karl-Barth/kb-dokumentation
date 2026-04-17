# `<title>` Titel

Titel mit verschiedenen Funktionen, unterschieden durch @type: Bandtitel (volume), inhaltlicher Titel (content), formaler Titel (formal), Zitierzeilen (citation_line_1–3), Editionstitel (edition) und Texttitel (text).

Die Attribute key und ref, die durch die Zugehörigkeit zur Klasse
      att.canonical verfügbar sind, können dafür verwendet werden, den
      kanonischen Titel anzugeben: Ersteres indem (z. B.) die Kennung eines Datensatzes einer externen
      Bibliothek herangezogen wird; Letzteres durch den Verweis auf ein XML-Element, das den
      kanonischen Titel enthält.

**Modul:** core — Kernmodule

## Attribute

**att.global** stellt gemeinsame Attribute für alle Elemente im TEI-Kodierungsschema bereit.

**@xml:id** (optional)
:   liefert einen Identifikator für das Element, welches dieses Attribut trägt.
:   Datentyp: ID

**@n** (optional)
:   gibt eine Nummer (oder eine andere Bezeichnung) für ein Element an, die innerhalb des Dokuments nicht zwangsläufig eindeutig ist.
:   Datentyp: teidata.text

**@xml:lang** (optional)
:   gibt die Sprache des Elementinhalts durch ein Tag an, das nach BCP 47 festgelegt wird.
:   Datentyp: teidata.language

**@xml:base** (optional)
:   liefert eine Basis-URI-Referenz, mit der Anwendungen relative URI-Referenzen in absolute auflösen können.
:   Datentyp: teidata.pointer

**@xml:space** (optional, geschlossene Werteliste)
:   signalisiert die gewünschte Handhabung von Leerzeichen durch Anwendungen.
:   Datentyp: teidata.enumerated
:   `default`
:   `preserve`


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


**@level** (optional, geschlossene Werteliste)
:   gibt den bibliografischen Typ eines Titels an, d.h. ob er einen Artikel, ein Buch, eine Zeitschrift, eine Reihe oder unpubliziertes Material bezeichnet.
:   Datentyp: teidata.enumerated
:   `a` — der Titel gehört zu einer unselbständigen Publikation, wie einem Artikel, Gedicht oder einem anderen Werk, das als Teil einer umfangreicheren Einheit publiziert wurde.
:   `m` — der Titel bezieht sich auf Monografien wie z.B. ein Bücher oder andere selbständige Publikationen, also auch auf einzelne Bände in einem mehrbändigen Werk.
:   `j` — der Titel bezieht sich auf jede Art fortlaufender oder periodischer Veröffentlichungen wie z. B. Zeitschriften, Magazine oder Zeitungen.
:   `s` — der Titel bezeichnet eine Reihe von ansonsten selbständig publizierten Veröffentlichungen, wie z. B. eine Buchreihe.
:   `u` — der Titel bezieht sich auf unveröffentliches Material (incl. universitäre Qualifikationsarbeiten, soweit sie nicht von einem Verlag veröffentlicht worden sind).

**@type** (optional, geschlossene Werteliste)
:   klassifiziert den Titel entsprechend einer geeigneten Typologie.
:   Datentyp: teidata.enumerated
:   `volume` — Bandtitel, z.B. Karl Barth - Rudolf Bultmann. Briefwechsel 1911-1966
:   `content` — Inhaltlicher Titel, z.B. «Karl Barth an Rudolf Bultmann»
:   `formal` — Formaler Titel (in einem Band), z.B. «Brief Nr. 4» oder «Vorwort»
:   `citation_line_1` — Titel für Zitierung (erste Zeile)
:   `citation_line_2` — Titel für Zitierung (zweite Zeile): Url mit Datum
:   `citation_line_3` — Titel für Zitierung (dritte Zeile): Angabe des Drucks
:   `edition` — Titel der Edition
:   `text` — Titel (verwendet als Angabe in der aps)
:   `addon` — Für Erweiterung des Titels


## Enthalten in

**header:** [titleStmt](titleStmt.md) "sollte mehrere Titel für verschiedene Zwecke enhalten."

## Beispiele

**Beispiel 1:**

```xml
<title type="volume" n="vol-01">Karl Barth – Rudolf Bultmann. Briefwechsel 1911–1966</title>
```

**Beispiel 2:**

```xml
<title type="content">Karl Barth an Rudolf Bultmann</title>
```

**Beispiel 3:**

```xml
<title type="citation_line_1">Karl Barth an Rudolf Bultmann, 16. Juli 1928</title>
```

## Content Model

```xml
<content>
  <macroRef key="macro.paraContent"/>
</content>
```
