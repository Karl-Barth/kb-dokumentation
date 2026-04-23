# `<docDate>` Datierung des Dokuments

enthält die Datierung des Dokuments, wie auf der Titelseite oder in einer Datumszeile angegeben.

Vgl. das allgemeine date-Element im core-Modul. Dieses
      spezialisierte Element erleichtert die Kodierung und Verarbeitung der Datierung eines Dokuments,
      die vermutlich in vielen Anwendungsszenarien gesondert behandelt wird. Es sollte nur für das
      Datum des gesamten Dokuments verwendet werden, nicht für Datierungen von Abschnitten oder
      Teilen.

[TEI Guidelines: docDate](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-docDate.html)

**Modul:** textstructure — Textstruktur

## Enthalten in

**textstructure:** [body](body.md) "Enthält den gesamten Textkörper eines KBGA-Dokuments." [dateline](dateline.md) "enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw." [div](div.md) "Gliederungseinheit eines Textes. Der @type unterscheidet Tex"

**core:** [lg](lg.md) "Strophe oder Versgruppe." [list](list.md) "Liste. Der @type unterscheidet geordnete und ungeordnete Lis"

**figures:** [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik (" [table](table.md) "Tabelle."

## Kann enthalten

Beliebiger Textinhalt

**core:** [abbr](abbr.md) "Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref" [address](address.md) "enthält eine Postadresse, z. B. eines Verlegers, einer Organ" [choice](choice.md) "Gruppiert sic/corr-Paare für Korrekturen der Druckausgabe." [cit](cit.md) "Zitat mit optionaler bibliographischer Angabe." [corr](corr.md) "Korrektur eines Fehlers in der Druckausgabe. Der @type unter" [date](date.md) "Datumsangabe mit maschinenlesbarem Datum in @when, @from/@to" [foreign](foreign.md) "Fremdsprachiger Text. Das @xml:lang gibt die Sprache an, @re" [graphic](graphic.md) "Verweis auf eine Bilddatei via @url." [hi](hi.md) "Hervorhebung. Das @rend gibt die Art an (italic, bold, sup, " [lb](lb.md) "markiert den Anfang einer neuen typographischen 
    Zeile i" [milestone](milestone.md) "markiert einen Grenzpunkt, der Abschnitte eines Textes trenn" [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [pb](pb.md) "Seitenumbruch. Das @ed unterscheidet die Ausgabe (pga, A), @" [ptr](ptr.md) "defines a pointer to another location." [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L" [rs](rs.md) "Referenzierende Zeichenkette für Akteure, die nicht als pers" [sic](sic.md) "Markiert die fehlerhafte Stelle in der Druckausgabe (innerha" [term](term.md) "Sachbegriff mit Verweis auf die Begriffs-Taxonomie via @ref " [title](title.md) "Titel mit verschiedenen Funktionen, unterschieden durch @typ"

**header:** [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer."

**linking:** [anchor](anchor.md) "Ankerpunkt für Querverweise (@type='cross') und für Fussnote" [seg](seg.md) "Segment. Verwendet für nicht-Entitäten, Verse, Biogramme, He"

**namesdates:** [orgName](orgName.md) "Name einer Organisation mit Verweis auf die Meta-DB via @ref" [persName](persName.md) "Personenname mit Verweis auf die Meta-DB via @ref (kbga-acto" [placeName](placeName.md) "Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-I"

**figures:** [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik ("

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
"

**analysis:** [span](span.md) "associates an interpretative annotation directly with a span"

## Content Model

```xml
<content>
    <macroRef key="macro.phraseSeq"/>
  </content>
```
