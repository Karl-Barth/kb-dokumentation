# `<bibl>` bibliografische Angabe

Bibliographische Angabe. Unterscheidet zwischen gedruckter Gesamtausgabe (pga), Alexander Street Press (asp), Quellen (source) und Liedern (song).

Siehe [Textelemente > Literatur](https://dokumentation.karl-barth.ch/textelemente/literatur/)

[TEI Guidelines: bibl](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-bibl.html)

**Modul:** core — Kernmodule

## Attribute

**@type** (optional)
:   `pga` — Printed Gesamtausgabe (Ausgabe des TVZ)
:   `asp` — Alexander Street Press (digital edition)
:   `source` — Quelle für einen Text der KBGA

**@subtype** (optional, geschlossene Werteliste)
:   Angabe der Funktion einer Quelle für den edierten Text
:   `Vorlage_der_Edition`
:   `Weitere_Vorlage`
:   `Material_zum_Kontext`
:   `rkg` — Gesangsbuch der evangelisch-reformierten Kirchen der deutschsprachigen Schweiz (1952)
:   `ekg` — Deutsches Evangelisches Kirchengesangbuch (1950)
:   `erkg` — Gesangbuch für die evangelisch-reformirte Kirche der deutschen Schweiz (1891)
:   `eg` — Evangelisches Gesangsbuch Deutschlands (1993ff.)
:   `rg` — Reformiertes Gesangsbuch der deutschsprachigen Schweiz (1998)
:   `reichslieder` — Reichs-Lieder. Deutsches Gemeinschafts-Liederbuch

**@n** (optional)
:   Bezeichnung der Quelle für einen edierten Text
:   Datentyp: string — Pattern: `[A-Z][0-9]?`

**@xml:id** (optional)
:   Datentyp: ID — Pattern: `(b[\-0-9]+|pga|asp|kbga-(sources|bibls|songs|actors|places|keywords)-[0-9]+|[A-Z]\d*)`

**@corresp** (optional)


## Enthalten in

**textstructure:** [argument](argument.md) "Zusammenfassung oder Regest eines Textes, typisch am Anfang " [body](body.md) "Enthält den gesamten Textkörper eines KBGA-Dokuments." [div](div.md) "Gliederungseinheit eines Textes. Der @type unterscheidet Tex" [epigraph](epigraph.md) "enthält ein anonymes oder jemandem zugeschriebenes Zitat, da" [postscript](postscript.md) "enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief." [salute](salute.md) "enthält eine Anrede oder Grußformel, die einem Vorwort, eine" [signed](signed.md) "enthält die abschließende Grußformel o.Ä. die ein Vorwort, e"

**core:** [bibl](bibl.md) "Bibliographische Angabe. Unterscheidet zwischen gedruckter G" [cit](cit.md) "Zitat mit optionaler bibliographischer Angabe." [corr](corr.md) "Korrektur eines Fehlers in der Druckausgabe. Der @type unter" [head](head.md) "Überschrift einer Gliederungseinheit (div)." [hi](hi.md) "Hervorhebung. Das @rend gibt die Art an (italic, bold, sup, " [item](item.md) "enthält einen Listenpunkt." [l](l.md) "Verszeile." [listBibl](listBibl.md) "enthält eine Liste von bibliografischen Angaben jeglicher Ar" [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo" [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L" [sic](sic.md) "Markiert die fehlerhafte Stelle in der Druckausgabe (innerha" [stage](stage.md) "enthält jegliche Regieanweisung in einem Dramentext oder -fr" [title](title.md) "Titel mit verschiedenen Funktionen, unterschieden durch @typ"

**header:** [change](change.md) "Änderungsvermerk in der revisionDesc. Enthält Zeitstempel de" [licence](licence.md) "beinhaltet für den Text gültige Lizenzinformationen oder and" [sourceDesc](sourceDesc.md) "beschreibt die Quelle, von der sich der elektronische Text a"

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati" [seg](seg.md) "Segment. Verwendet für nicht-Entitäten, Verse, Biogramme, He"

**namesdates:** [event](event.md) "enthält Daten mit Bezug zu etwas Bemerkenswertem, das in der"

**figures:** [cell](cell.md) "Tabellenzelle." [figDesc](figDesc.md) "enthält einen kurzen Beschreibungstext des Inhalts oder des " [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik ("

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
"

## Kann enthalten

Beliebiger Textinhalt

**core:** [abbr](abbr.md) "Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref" [address](address.md) "enthält eine Postadresse, z. B. eines Verlegers, einer Organ" [author](author.md) "Verfasserangabe im teiHeader. Das @ref verweist auf die Pers" [bibl](bibl.md) "Bibliographische Angabe. Unterscheidet zwischen gedruckter G" [biblScope](biblScope.md) "Umfangsangabe innerhalb einer bibliographischen Referenz (Se" [choice](choice.md) "Gruppiert sic/corr-Paare für Korrekturen der Druckausgabe." [corr](corr.md) "Korrektur eines Fehlers in der Druckausgabe. Der @type unter" [date](date.md) "Datumsangabe mit maschinenlesbarem Datum in @when, @from/@to" [editor](editor.md) "Herausgeberangabe in einer bibliographischen Referenz." [foreign](foreign.md) "Fremdsprachiger Text. Das @xml:lang gibt die Sprache an, @re" [hi](hi.md) "Hervorhebung. Das @rend gibt die Art an (italic, bold, sup, " [lb](lb.md) "markiert den Anfang einer neuen typographischen 
    Zeile i" [milestone](milestone.md) "markiert einen Grenzpunkt, der Abschnitte eines Textes trenn" [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [pb](pb.md) "Seitenumbruch. Das @ed unterscheidet die Ausgabe (pga, A), @" [ptr](ptr.md) "defines a pointer to another location." [pubPlace](pubPlace.md) "enthält den Namen des Orts, an dem ein bibliografisches Obje" [publisher](publisher.md) "gibt den Namen der Organisation an, die für die Veröffentlic" [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L" [rs](rs.md) "Referenzierende Zeichenkette für Akteure, die nicht als pers" [sic](sic.md) "Markiert die fehlerhafte Stelle in der Druckausgabe (innerha" [term](term.md) "Sachbegriff mit Verweis auf die Begriffs-Taxonomie via @ref " [title](title.md) "Titel mit verschiedenen Funktionen, unterschieden durch @typ"

**header:** [availability](availability.md) "Lizenzinformationen zur Publikation. Wird aus der Datenbank " [edition](edition.md) "beschreibt die Details einer Ausgabe eines Textes." [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer." [sponsor](sponsor.md) "gibt den Namen einer Organisation oder Institution an, die a"

**linking:** [anchor](anchor.md) "Ankerpunkt für Querverweise (@type='cross') und für Fussnote" [seg](seg.md) "Segment. Verwendet für nicht-Entitäten, Verse, Biogramme, He"

**namesdates:** [orgName](orgName.md) "Name einer Organisation mit Verweis auf die Meta-DB via @ref" [persName](persName.md) "Personenname mit Verweis auf die Meta-DB via @ref (kbga-acto" [placeName](placeName.md) "Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-I"

**figures:** [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik ("

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
"

**analysis:** [span](span.md) "associates an interpretative annotation directly with a span"

## Constraints

**song1**
:   song1: bibl[@type='song'] muss @corresp enthalten.

**song2**
:   song2: bibl[@type='song'] darf keinen @subtype enthalten.

## Beispiele

```xml
<bibl type="source">A (Vorlage der Edition): Bultmann, Rudolf, Rudolf Bultmann an Karl Barth, 11. Juni 1911. <ref target="https://kba.karl-barth.ch/objects/7950">KBA 9311.73</ref>.</bibl>
```

## Content Model

```xml
<content>
  <alternate minOccurs="0" maxOccurs="unbounded">
    <textNode/>
    <classRef key="model.gLike"/>
    <classRef key="model.highlighted"/>
    <classRef key="model.pPart.data"/>
    <classRef key="model.pPart.edit"/>
    <classRef key="model.segLike"/>
    <classRef key="model.ptrLike"/>
    <classRef key="model.biblPart"/>
    <classRef key="model.global"/>
  </alternate>
</content>
```
