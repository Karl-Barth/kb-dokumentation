# `<p>` Absatz

Absatz. Darf nicht verschachtelt werden (ausser innerhalb von note).

Siehe [Textstruktur > Absatz](https://dokumentation.karl-barth.ch/textstruktur/absatz/)

[TEI Guidelines: p](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-p.html)

**Modul:** core — Kernmodule

## Attribute

**@corresp** (optional)

**@n** (optional)

**@rend** (optional)

**@xml:id** (optional)

**@xml:lang** (optional)


## Enthalten in

**textstructure:** [argument](argument.md) "Zusammenfassung oder Regest eines Textes, typisch am Anfang " [body](body.md) "Enthält den gesamten Textkörper eines KBGA-Dokuments." [div](div.md) "Gliederungseinheit eines Textes. Der @type unterscheidet Tex" [epigraph](epigraph.md) "enthält ein anonymes oder jemandem zugeschriebenes Zitat, da" [postscript](postscript.md) "enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief."

**core:** [item](item.md) "enthält einen Listenpunkt." [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [sp](sp.md) "enthält eine einzelne Figurenrede in einem Dramentext oder e" [stage](stage.md) "enthält jegliche Regieanweisung in einem Dramentext oder -fr"

**header:** [availability](availability.md) "Lizenzinformationen zur Publikation. Wird aus der Datenbank " [change](change.md) "Änderungsvermerk in der revisionDesc. Enthält Zeitstempel de" [correspAction](correspAction.md) "contains a structured
  description of the place, the name o" [correspContext](correspContext.md) "provides references to preceding or following correspondence" [correspDesc](correspDesc.md) "contains a description
    of the actions related to one act" [editionStmt](editionStmt.md) "Angaben zur digitalen Edition (Titel, Förderer)." [encodingDesc](encodingDesc.md) "dokumentiert das Verhältnis zwischen dem elektronischen Text" [langUsage](langUsage.md) "beschreibt Sprachen, Subsprachen, Register, Dialekte usw., d" [licence](licence.md) "beinhaltet für den Text gültige Lizenzinformationen oder and" [prefixDef](prefixDef.md) "defines a prefixing scheme used in teidata.pointer values,
 " [publicationStmt](publicationStmt.md) "umfasst Angaben zu Veröffentlichung oder Vertrieb eines elek" [sourceDesc](sourceDesc.md) "beschreibt die Quelle, von der sich der elektronische Text a"

**namesdates:** [event](event.md) "enthält Daten mit Bezug zu etwas Bemerkenswertem, das in der"

**figures:** [cell](cell.md) "Tabellenzelle." [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik ("

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
"

## Kann enthalten

Beliebiger Textinhalt

**core:** [abbr](abbr.md) "Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref" [address](address.md) "enthält eine Postadresse, z. B. eines Verlegers, einer Organ" [bibl](bibl.md) "Bibliographische Angabe. Unterscheidet zwischen gedruckter G" [choice](choice.md) "Gruppiert sic/corr-Paare für Korrekturen der Druckausgabe." [cit](cit.md) "Zitat mit optionaler bibliographischer Angabe." [corr](corr.md) "Korrektur eines Fehlers in der Druckausgabe. Der @type unter" [date](date.md) "Datumsangabe mit maschinenlesbarem Datum in @when, @from/@to" [foreign](foreign.md) "Fremdsprachiger Text. Das @xml:lang gibt die Sprache an, @re" [graphic](graphic.md) "Verweis auf eine Bilddatei via @url." [hi](hi.md) "Hervorhebung. Das @rend gibt die Art an (italic, bold, sup, " [l](l.md) "Verszeile." [lb](lb.md) "markiert den Anfang einer neuen typographischen 
    Zeile i" [lg](lg.md) "Strophe oder Versgruppe." [list](list.md) "Liste. Der @type unterscheidet geordnete und ungeordnete Lis" [listBibl](listBibl.md) "enthält eine Liste von bibliografischen Angaben jeglicher Ar" [milestone](milestone.md) "markiert einen Grenzpunkt, der Abschnitte eines Textes trenn" [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [pb](pb.md) "Seitenumbruch. Das @ed unterscheidet die Ausgabe (pga, A), @" [ptr](ptr.md) "defines a pointer to another location." [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L" [rs](rs.md) "Referenzierende Zeichenkette für Akteure, die nicht als pers" [sic](sic.md) "Markiert die fehlerhafte Stelle in der Druckausgabe (innerha" [stage](stage.md) "enthält jegliche Regieanweisung in einem Dramentext oder -fr" [term](term.md) "Sachbegriff mit Verweis auf die Begriffs-Taxonomie via @ref " [title](title.md) "Titel mit verschiedenen Funktionen, unterschieden durch @typ"

**header:** [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer."

**linking:** [anchor](anchor.md) "Ankerpunkt für Querverweise (@type='cross') und für Fussnote" [seg](seg.md) "Segment. Verwendet für nicht-Entitäten, Verse, Biogramme, He"

**namesdates:** [listEvent](listEvent.md) "contains a list of descriptions, each of which provides info" [orgName](orgName.md) "Name einer Organisation mit Verweis auf die Meta-DB via @ref" [persName](persName.md) "Personenname mit Verweis auf die Meta-DB via @ref (kbga-acto" [placeName](placeName.md) "Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-I"

**figures:** [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik (" [table](table.md) "Tabelle."

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
"

**analysis:** [span](span.md) "associates an interpretative annotation directly with a span"

## Constraints

**p1**
:   p1: p darf nicht in p vorkommen (Ausnahme in note).

**abstractModel-structure-p-in-ab-or-p**
:   Abstract model violation: Paragraphs may not occur inside other paragraphs or ab elements.

**abstractModel-structure-p-in-l**
:   Abstract model violation: Metrical lines may not contain higher-level structural elements such as div, p, or ab, unless p is a child of figure or note, or is a descendant of floatingText.

## Beispiele

```xml
<p>Gottes Gebot geht mich an, sofern ich als Christ ein Glied
  seines auserwählten Volkes bin.</p>
```

## Content Model

```xml
<content>
  <macroRef key="macro.paraContent"/>
</content>
```
