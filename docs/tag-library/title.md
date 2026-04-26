# `<title>` Titel

Titel mit verschiedenen Funktionen, unterschieden durch @type: Bandtitel (volume), inhaltlicher Titel (content), formaler Titel (formal), Zitierzeilen (citation_line_1–3), Editionstitel (edition) und Texttitel (text).

Die Attribute key und ref, die durch die Zugehörigkeit zur Klasse
      att.canonical verfügbar sind, können dafür verwendet werden, den
      kanonischen Titel anzugeben: Ersteres indem (z. B.) die Kennung eines Datensatzes einer externen
      Bibliothek herangezogen wird; Letzteres durch den Verweis auf ein XML-Element, das den
      kanonischen Titel enthält.

[TEI Guidelines: title](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-title.html)

**Modul:** core — Kernmodule

## Attribute

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

**@n** (optional)

**@rend** (optional)

**@xml:lang** (optional)


## Enthalten in

**textstructure:** [closer](closer.md) "Schlussformel eines Briefes (Gruss, Unterschrift, Datum)." [dateline](dateline.md) "enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw." [docDate](docDate.md) "enthält die Datierung des Dokuments, wie auf der Titelseite " [opener](opener.md) "fasst Datumszeile, Verfasserangabe, Anredeformel und ähnlich" [salute](salute.md) "enthält eine Anrede oder Grußformel, die einem Vorwort, eine" [signed](signed.md) "enthält die abschließende Grußformel o.Ä. die ein Vorwort, e"

**core:** [abbr](abbr.md) "Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref" [addrLine](addrLine.md) "enthält eine Zeile einer Postadresse." [author](author.md) "Verfasserangabe im teiHeader. Das @ref verweist auf die Pers" [bibl](bibl.md) "Bibliographische Angabe. Unterscheidet zwischen gedruckter G" [biblScope](biblScope.md) "Umfangsangabe innerhalb einer bibliographischen Referenz (Se" [corr](corr.md) "Korrektur eines Fehlers in der Druckausgabe. Der @type unter" [date](date.md) "Datumsangabe mit maschinenlesbarem Datum in @when, @from/@to" [editor](editor.md) "Herausgeberangabe in einer bibliographischen Referenz." [foreign](foreign.md) "Fremdsprachiger Text. Das @xml:lang gibt die Sprache an, @re" [head](head.md) "Überschrift einer Gliederungseinheit (div)." [hi](hi.md) "Hervorhebung. Das @rend gibt die Art an (italic, bold, sup, " [item](item.md) "enthält einen Listenpunkt." [l](l.md) "Verszeile." [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo" [pubPlace](pubPlace.md) "enthält den Namen des Orts, an dem ein bibliografisches Obje" [publisher](publisher.md) "gibt den Namen der Organisation an, die für die Veröffentlic" [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L" [rs](rs.md) "Referenzierende Zeichenkette für Akteure, die nicht als pers" [sic](sic.md) "Markiert die fehlerhafte Stelle in der Druckausgabe (innerha" [speaker](speaker.md) "enthält eine spezielle Form von Überschrift oder Bezeichnung" [stage](stage.md) "enthält jegliche Regieanweisung in einem Dramentext oder -fr" [term](term.md) "Sachbegriff mit Verweis auf die Begriffs-Taxonomie via @ref " [title](title.md) "Titel mit verschiedenen Funktionen, unterschieden durch @typ"

**header:** [change](change.md) "Änderungsvermerk in der revisionDesc. Enthält Zeitstempel de" [creation](creation.md) "beinhaltet Informationen zur Entstehung eines Textes." [edition](edition.md) "beschreibt die Details einer Ausgabe eines Textes." [language](language.md) "beschreibt eine einzelne Sprache oder eine Subsprache, die i" [licence](licence.md) "beinhaltet für den Text gültige Lizenzinformationen oder and" [sponsor](sponsor.md) "gibt den Namen einer Organisation oder Institution an, die a" [titleStmt](titleStmt.md) "sollte mehrere Titel für verschiedene Zwecke enhalten."

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati" [seg](seg.md) "Segment. Verwendet für nicht-Entitäten, Verse, Biogramme, He"

**namesdates:** [orgName](orgName.md) "Name einer Organisation mit Verweis auf die Meta-DB via @ref" [persName](persName.md) "Personenname mit Verweis auf die Meta-DB via @ref (kbga-acto" [placeName](placeName.md) "Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-I"

**figures:** [cell](cell.md) "Tabellenzelle." [figDesc](figDesc.md) "enthält einen kurzen Beschreibungstext des Inhalts oder des "

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
" [supplied](supplied.md) "Editorische Ergaenzung. Das @source unterscheidet die Quelle"

**analysis:** [span](span.md) "associates an interpretative annotation directly with a span"

## Kann enthalten

Beliebiger Textinhalt

**core:** [abbr](abbr.md) "Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref" [address](address.md) "enthält eine Postadresse, z. B. eines Verlegers, einer Organ" [bibl](bibl.md) "Bibliographische Angabe. Unterscheidet zwischen gedruckter G" [choice](choice.md) "Gruppiert sic/corr-Paare für Korrekturen der Druckausgabe." [cit](cit.md) "Zitat mit optionaler bibliographischer Angabe." [corr](corr.md) "Korrektur eines Fehlers in der Druckausgabe. Der @type unter" [date](date.md) "Datumsangabe mit maschinenlesbarem Datum in @when, @from/@to" [foreign](foreign.md) "Fremdsprachiger Text. Das @xml:lang gibt die Sprache an, @re" [graphic](graphic.md) "Verweis auf eine Bilddatei via @url." [hi](hi.md) "Hervorhebung. Das @rend gibt die Art an (italic, bold, sup, " [l](l.md) "Verszeile." [lb](lb.md) "markiert den Anfang einer neuen typographischen 
    Zeile i" [lg](lg.md) "Strophe oder Versgruppe." [list](list.md) "Liste. Der @type unterscheidet geordnete und ungeordnete Lis" [listBibl](listBibl.md) "enthält eine Liste von bibliografischen Angaben jeglicher Ar" [milestone](milestone.md) "markiert einen Grenzpunkt, der Abschnitte eines Textes trenn" [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [pb](pb.md) "Seitenumbruch. Das @ed unterscheidet die Ausgabe (pga, A), @" [ptr](ptr.md) "defines a pointer to another location." [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L" [rs](rs.md) "Referenzierende Zeichenkette für Akteure, die nicht als pers" [sic](sic.md) "Markiert die fehlerhafte Stelle in der Druckausgabe (innerha" [stage](stage.md) "enthält jegliche Regieanweisung in einem Dramentext oder -fr" [term](term.md) "Sachbegriff mit Verweis auf die Begriffs-Taxonomie via @ref " [title](title.md) "Titel mit verschiedenen Funktionen, unterschieden durch @typ"

**header:** [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer."

**linking:** [anchor](anchor.md) "Ankerpunkt für Querverweise (@type='cross') und für Fussnote" [seg](seg.md) "Segment. Verwendet für nicht-Entitäten, Verse, Biogramme, He"

**namesdates:** [listEvent](listEvent.md) "contains a list of descriptions, each of which provides info" [orgName](orgName.md) "Name einer Organisation mit Verweis auf die Meta-DB via @ref" [persName](persName.md) "Personenname mit Verweis auf die Meta-DB via @ref (kbga-acto" [placeName](placeName.md) "Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-I"

**figures:** [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik (" [table](table.md) "Tabelle."

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
" [supplied](supplied.md) "Editorische Ergaenzung. Das @source unterscheidet die Quelle"

**analysis:** [span](span.md) "associates an interpretative annotation directly with a span"

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
