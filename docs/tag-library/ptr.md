# `<ptr>`

defines a pointer to another location.

Die target und cRef-Attribute schließen sich gegenseitig aus.

Siehe [Textstruktur > Anmerkungen](https://dokumentation.karl-barth.ch/textstruktur/anmerkungen/)

[TEI Guidelines: ptr](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-ptr.html)

**Modul:** core — Kernmodule

## Attribute

**@n** (optional)

**@target** (optional)

**@type** (optional)

**@xml:id** (optional)


## Enthalten in

**textstructure:** [closer](closer.md) "Schlussformel eines Briefes (Gruss, Unterschrift, Datum)." [dateline](dateline.md) "enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw." [docDate](docDate.md) "enthält die Datierung des Dokuments, wie auf der Titelseite " [opener](opener.md) "fasst Datumszeile, Verfasserangabe, Anredeformel und ähnlich" [salute](salute.md) "enthält eine Anrede oder Grußformel, die einem Vorwort, eine" [signed](signed.md) "enthält die abschließende Grußformel o.Ä. die ein Vorwort, e"

**core:** [abbr](abbr.md) "Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref" [addrLine](addrLine.md) "enthält eine Zeile einer Postadresse." [author](author.md) "Verfasserangabe im teiHeader. Das @ref verweist auf die Pers" [bibl](bibl.md) "Bibliographische Angabe. Unterscheidet zwischen gedruckter G" [biblScope](biblScope.md) "Umfangsangabe innerhalb einer bibliographischen Referenz (Se" [cit](cit.md) "Zitat mit optionaler bibliographischer Angabe." [corr](corr.md) "Korrektur eines Fehlers in der Druckausgabe. Der @type unter" [date](date.md) "Datumsangabe mit maschinenlesbarem Datum in @when, @from/@to" [editor](editor.md) "Herausgeberangabe in einer bibliographischen Referenz." [foreign](foreign.md) "Fremdsprachiger Text. Das @xml:lang gibt die Sprache an, @re" [head](head.md) "Überschrift einer Gliederungseinheit (div)." [hi](hi.md) "Hervorhebung. Das @rend gibt die Art an (italic, bold, sup, " [item](item.md) "enthält einen Listenpunkt." [l](l.md) "Verszeile." [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo" [pubPlace](pubPlace.md) "enthält den Namen des Orts, an dem ein bibliografisches Obje" [publisher](publisher.md) "gibt den Namen der Organisation an, die für die Veröffentlic" [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L" [rs](rs.md) "Referenzierende Zeichenkette für Akteure, die nicht als pers" [sic](sic.md) "Markiert die fehlerhafte Stelle in der Druckausgabe (innerha" [speaker](speaker.md) "enthält eine spezielle Form von Überschrift oder Bezeichnung" [stage](stage.md) "enthält jegliche Regieanweisung in einem Dramentext oder -fr" [term](term.md) "Sachbegriff mit Verweis auf die Begriffs-Taxonomie via @ref " [title](title.md) "Titel mit verschiedenen Funktionen, unterschieden durch @typ"

**header:** [change](change.md) "Änderungsvermerk in der revisionDesc. Enthält Zeitstempel de" [correspContext](correspContext.md) "provides references to preceding or following correspondence" [creation](creation.md) "beinhaltet Informationen zur Entstehung eines Textes." [edition](edition.md) "beschreibt die Details einer Ausgabe eines Textes." [language](language.md) "beschreibt eine einzelne Sprache oder eine Subsprache, die i" [licence](licence.md) "beinhaltet für den Text gültige Lizenzinformationen oder and" [publicationStmt](publicationStmt.md) "umfasst Angaben zu Veröffentlichung oder Vertrieb eines elek" [sponsor](sponsor.md) "gibt den Namen einer Organisation oder Institution an, die a"

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati" [seg](seg.md) "Segment. Verwendet für nicht-Entitäten, Verse, Biogramme, He"

**namesdates:** [event](event.md) "enthält Daten mit Bezug zu etwas Bemerkenswertem, das in der" [orgName](orgName.md) "Name einer Organisation mit Verweis auf die Meta-DB via @ref" [persName](persName.md) "Personenname mit Verweis auf die Meta-DB via @ref (kbga-acto" [placeName](placeName.md) "Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-I"

**figures:** [cell](cell.md) "Tabellenzelle." [figDesc](figDesc.md) "enthält einen kurzen Beschreibungstext des Inhalts oder des "

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
"

**analysis:** [span](span.md) "associates an interpretative annotation directly with a span"

## Kann enthalten

Leeres Element.

## Constraints

**ptrAtts**
:   Only one of the attributes @target and @cRef may be supplied on .

## Content Model

```xml
<content>
  <empty/>
</content>
```
