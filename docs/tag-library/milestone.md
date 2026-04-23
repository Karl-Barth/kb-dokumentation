# `<milestone>` Grenzpunkt

markiert einen Grenzpunkt, der Abschnitte eines Textes trennen kann, 
    typischerweise (aber nicht notwendigerweise) den Wechsel eines Bezugssystems, 
    der nicht durch ein strukturelles Markup beschrieben werden kann.

Das globale n-Attribut gibt für dieses Element die neue Zahl 
      (oder einen anderen Wert) der Einheit an, die an diesem Grenzpunkt wechselt. 
      Der besondere Wert unnumbered (ungezählt) sollte für Abschnitte gewählt werden, 
      die außerhalb des normalen Zählsystems fallen, wie beispielsweise Kapitel- 
      oder andere Überschriften, Gedichtnummern oder -titel etc.
    Die Reihenfolge des Auftretens von mehreren milestone-Elementen 
      an einem gegebenen Punkt ist normalerweise nicht signifikant.

[TEI Guidelines: milestone](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-milestone.html)

**Modul:** core — Kernmodule

## Attribute

**@unit** (optional)

**@xml:id** (optional)


## Enthalten in

**textstructure:** [argument](argument.md) "Zusammenfassung oder Regest eines Textes, typisch am Anfang " [body](body.md) "Enthält den gesamten Textkörper eines KBGA-Dokuments." [closer](closer.md) "Schlussformel eines Briefes (Gruss, Unterschrift, Datum)." [dateline](dateline.md) "enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw." [div](div.md) "Gliederungseinheit eines Textes. Der @type unterscheidet Tex" [docDate](docDate.md) "enthält die Datierung des Dokuments, wie auf der Titelseite " [epigraph](epigraph.md) "enthält ein anonymes oder jemandem zugeschriebenes Zitat, da" [opener](opener.md) "fasst Datumszeile, Verfasserangabe, Anredeformel und ähnlich" [postscript](postscript.md) "enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief." [salute](salute.md) "enthält eine Anrede oder Grußformel, die einem Vorwort, eine" [signed](signed.md) "enthält die abschließende Grußformel o.Ä. die ein Vorwort, e" [text](text.md) "enthält einen einzelnen, eigenständigen oder kompilierten Te"

**core:** [abbr](abbr.md) "Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref" [addrLine](addrLine.md) "enthält eine Zeile einer Postadresse." [address](address.md) "enthält eine Postadresse, z. B. eines Verlegers, einer Organ" [author](author.md) "Verfasserangabe im teiHeader. Das @ref verweist auf die Pers" [bibl](bibl.md) "Bibliographische Angabe. Unterscheidet zwischen gedruckter G" [biblScope](biblScope.md) "Umfangsangabe innerhalb einer bibliographischen Referenz (Se" [cit](cit.md) "Zitat mit optionaler bibliographischer Angabe." [corr](corr.md) "Korrektur eines Fehlers in der Druckausgabe. Der @type unter" [date](date.md) "Datumsangabe mit maschinenlesbarem Datum in @when, @from/@to" [editor](editor.md) "Herausgeberangabe in einer bibliographischen Referenz." [foreign](foreign.md) "Fremdsprachiger Text. Das @xml:lang gibt die Sprache an, @re" [head](head.md) "Überschrift einer Gliederungseinheit (div)." [hi](hi.md) "Hervorhebung. Das @rend gibt die Art an (italic, bold, sup, " [item](item.md) "enthält einen Listenpunkt." [l](l.md) "Verszeile." [lg](lg.md) "Strophe oder Versgruppe." [list](list.md) "Liste. Der @type unterscheidet geordnete und ungeordnete Lis" [listBibl](listBibl.md) "enthält eine Liste von bibliografischen Angaben jeglicher Ar" [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo" [pubPlace](pubPlace.md) "enthält den Namen des Orts, an dem ein bibliografisches Obje" [publisher](publisher.md) "gibt den Namen der Organisation an, die für die Veröffentlic" [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L" [rs](rs.md) "Referenzierende Zeichenkette für Akteure, die nicht als pers" [sic](sic.md) "Markiert die fehlerhafte Stelle in der Druckausgabe (innerha" [sp](sp.md) "enthält eine einzelne Figurenrede in einem Dramentext oder e" [speaker](speaker.md) "enthält eine spezielle Form von Überschrift oder Bezeichnung" [stage](stage.md) "enthält jegliche Regieanweisung in einem Dramentext oder -fr" [term](term.md) "Sachbegriff mit Verweis auf die Begriffs-Taxonomie via @ref " [title](title.md) "Titel mit verschiedenen Funktionen, unterschieden durch @typ"

**header:** [change](change.md) "Änderungsvermerk in der revisionDesc. Enthält Zeitstempel de" [edition](edition.md) "beschreibt die Details einer Ausgabe eines Textes." [language](language.md) "beschreibt eine einzelne Sprache oder eine Subsprache, die i" [licence](licence.md) "beinhaltet für den Text gültige Lizenzinformationen oder and" [sponsor](sponsor.md) "gibt den Namen einer Organisation oder Institution an, die a"

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati" [seg](seg.md) "Segment. Verwendet für nicht-Entitäten, Verse, Biogramme, He"

**namesdates:** [orgName](orgName.md) "Name einer Organisation mit Verweis auf die Meta-DB via @ref" [persName](persName.md) "Personenname mit Verweis auf die Meta-DB via @ref (kbga-acto" [placeName](placeName.md) "Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-I"

**figures:** [cell](cell.md) "Tabellenzelle." [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik (" [table](table.md) "Tabelle."

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
"

**analysis:** [span](span.md) "associates an interpretative annotation directly with a span"

## Kann enthalten

Leeres Element.

## Content Model

```xml
<content>
  <empty/>
</content>
```
