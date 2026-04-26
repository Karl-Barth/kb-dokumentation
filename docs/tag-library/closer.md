# `<closer>`

Schlussformel eines Briefes (Gruss, Unterschrift, Datum).

Siehe [Textstruktur > Dateline](https://dokumentation.karl-barth.ch/textstruktur/dateline/)

[TEI Guidelines: closer](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-closer.html)

**Modul:** textstructure — Textstruktur

## Enthalten in

**textstructure:** [body](body.md) "Enthält den gesamten Textkörper eines KBGA-Dokuments." [div](div.md) "Gliederungseinheit eines Textes. Der @type unterscheidet Tex" [postscript](postscript.md) "enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief."

**core:** [lg](lg.md) "Strophe oder Versgruppe." [list](list.md) "Liste. Der @type unterscheidet geordnete und ungeordnete Lis"

**figures:** [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik (" [table](table.md) "Tabelle."

## Kann enthalten

Beliebiger Textinhalt

**textstructure:** [dateline](dateline.md) "enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw." [salute](salute.md) "enthält eine Anrede oder Grußformel, die einem Vorwort, eine" [signed](signed.md) "enthält die abschließende Grußformel o.Ä. die ein Vorwort, e"

**core:** [abbr](abbr.md) "Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref" [address](address.md) "enthält eine Postadresse, z. B. eines Verlegers, einer Organ" [choice](choice.md) "Gruppiert sic/corr-Paare für Korrekturen der Druckausgabe." [corr](corr.md) "Korrektur eines Fehlers in der Druckausgabe. Der @type unter" [date](date.md) "Datumsangabe mit maschinenlesbarem Datum in @when, @from/@to" [foreign](foreign.md) "Fremdsprachiger Text. Das @xml:lang gibt die Sprache an, @re" [graphic](graphic.md) "Verweis auf eine Bilddatei via @url." [hi](hi.md) "Hervorhebung. Das @rend gibt die Art an (italic, bold, sup, " [lb](lb.md) "markiert den Anfang einer neuen typographischen 
    Zeile i" [milestone](milestone.md) "markiert einen Grenzpunkt, der Abschnitte eines Textes trenn" [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [pb](pb.md) "Seitenumbruch. Das @ed unterscheidet die Ausgabe (pga, A), @" [ptr](ptr.md) "defines a pointer to another location." [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L" [rs](rs.md) "Referenzierende Zeichenkette für Akteure, die nicht als pers" [sic](sic.md) "Markiert die fehlerhafte Stelle in der Druckausgabe (innerha" [term](term.md) "Sachbegriff mit Verweis auf die Begriffs-Taxonomie via @ref " [title](title.md) "Titel mit verschiedenen Funktionen, unterschieden durch @typ"

**header:** [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer."

**linking:** [anchor](anchor.md) "Ankerpunkt für Querverweise (@type='cross') und für Fussnote" [seg](seg.md) "Segment. Verwendet für nicht-Entitäten, Verse, Biogramme, He"

**namesdates:** [orgName](orgName.md) "Name einer Organisation mit Verweis auf die Meta-DB via @ref" [persName](persName.md) "Personenname mit Verweis auf die Meta-DB via @ref (kbga-acto" [placeName](placeName.md) "Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-I"

**figures:** [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik ("

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
"

**analysis:** [span](span.md) "associates an interpretative annotation directly with a span"

## Beispiele

```xml
<closer>
    <salute>Mit herzlichem Gruß</salute>
    <salute>Ihr</salute>
    <signed>
      <persName ref="kbga-actors-512">Rudolf Bultmann</persName>
    </signed>
  </closer>
```

## Content Model

```xml
<content>
  <alternate minOccurs="0" maxOccurs="unbounded">
    <textNode/>
    <classRef key="model.gLike"/>
    <elementRef key="byline"/>
    <elementRef key="signed"/>
    <elementRef key="dateline"/>
    <elementRef key="salute"/>
    <classRef key="model.phrase"/>
    <classRef key="model.global"/>
  </alternate>
</content>
```
