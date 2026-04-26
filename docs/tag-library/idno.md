# `<idno>` Identifikator

Identifikator, z.B. URL oder KBA-Objektnummer.

Siehe [Textelemente > Querverweise](https://dokumentation.karl-barth.ch/textelemente/querverweise/)

[TEI Guidelines: idno](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-idno.html)

**Modul:** header — Header

## Attribute

**@xml:id** (optional)

**@type** (optional, erweiterbar)
:   bestimmt die Art des Identifikators (z. B. ISBN, Sozialversicherungsnummer, URI)
:   Datentyp: teidata.enumerated
:   `ISBN`
:   `ISSN`
:   `DOI`
:   `URI`
:   `VIAF`
:   `ESTC`
:   `OCLC`

**@rend** (optional)


## Enthalten in

**textstructure:** [closer](closer.md) "Schlussformel eines Briefes (Gruss, Unterschrift, Datum)." [dateline](dateline.md) "enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw." [docDate](docDate.md) "enthält die Datierung des Dokuments, wie auf der Titelseite " [opener](opener.md) "fasst Datumszeile, Verfasserangabe, Anredeformel und ähnlich" [salute](salute.md) "enthält eine Anrede oder Grußformel, die einem Vorwort, eine" [signed](signed.md) "enthält die abschließende Grußformel o.Ä. die ein Vorwort, e"

**core:** [abbr](abbr.md) "Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref" [addrLine](addrLine.md) "enthält eine Zeile einer Postadresse." [address](address.md) "enthält eine Postadresse, z. B. eines Verlegers, einer Organ" [author](author.md) "Verfasserangabe im teiHeader. Das @ref verweist auf die Pers" [bibl](bibl.md) "Bibliographische Angabe. Unterscheidet zwischen gedruckter G" [biblScope](biblScope.md) "Umfangsangabe innerhalb einer bibliographischen Referenz (Se" [corr](corr.md) "Korrektur eines Fehlers in der Druckausgabe. Der @type unter" [date](date.md) "Datumsangabe mit maschinenlesbarem Datum in @when, @from/@to" [editor](editor.md) "Herausgeberangabe in einer bibliographischen Referenz." [foreign](foreign.md) "Fremdsprachiger Text. Das @xml:lang gibt die Sprache an, @re" [head](head.md) "Überschrift einer Gliederungseinheit (div)." [hi](hi.md) "Hervorhebung. Das @rend gibt die Art an (italic, bold, sup, " [item](item.md) "enthält einen Listenpunkt." [l](l.md) "Verszeile." [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo" [pubPlace](pubPlace.md) "enthält den Namen des Orts, an dem ein bibliografisches Obje" [publisher](publisher.md) "gibt den Namen der Organisation an, die für die Veröffentlic" [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L" [rs](rs.md) "Referenzierende Zeichenkette für Akteure, die nicht als pers" [sic](sic.md) "Markiert die fehlerhafte Stelle in der Druckausgabe (innerha" [speaker](speaker.md) "enthält eine spezielle Form von Überschrift oder Bezeichnung" [stage](stage.md) "enthält jegliche Regieanweisung in einem Dramentext oder -fr" [term](term.md) "Sachbegriff mit Verweis auf die Begriffs-Taxonomie via @ref " [title](title.md) "Titel mit verschiedenen Funktionen, unterschieden durch @typ"

**header:** [change](change.md) "Änderungsvermerk in der revisionDesc. Enthält Zeitstempel de" [correspAction](correspAction.md) "contains a structured
  description of the place, the name o" [creation](creation.md) "beinhaltet Informationen zur Entstehung eines Textes." [edition](edition.md) "beschreibt die Details einer Ausgabe eines Textes." [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer." [language](language.md) "beschreibt eine einzelne Sprache oder eine Subsprache, die i" [licence](licence.md) "beinhaltet für den Text gültige Lizenzinformationen oder and" [publicationStmt](publicationStmt.md) "umfasst Angaben zu Veröffentlichung oder Vertrieb eines elek" [sponsor](sponsor.md) "gibt den Namen einer Organisation oder Institution an, die a"

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati" [seg](seg.md) "Segment. Verwendet für nicht-Entitäten, Verse, Biogramme, He"

**namesdates:** [event](event.md) "enthält Daten mit Bezug zu etwas Bemerkenswertem, das in der" [orgName](orgName.md) "Name einer Organisation mit Verweis auf die Meta-DB via @ref" [persName](persName.md) "Personenname mit Verweis auf die Meta-DB via @ref (kbga-acto" [placeName](placeName.md) "Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-I"

**figures:** [cell](cell.md) "Tabellenzelle." [figDesc](figDesc.md) "enthält einen kurzen Beschreibungstext des Inhalts oder des "

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
" [supplied](supplied.md) "Editorische Ergaenzung. Das @source unterscheidet die Quelle"

**analysis:** [span](span.md) "associates an interpretative annotation directly with a span"

## Kann enthalten

Beliebiger Textinhalt

**header:** [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer."

## Beispiele

```xml
<idno type="ISBN">978-1-906964-22-1</idno>
<idno type="ISSN">0143-3385</idno>
<idno type="DOI">10.1000/123</idno>
<idno type="URI">http://www.worldcat.org/oclc/185922478</idno>
<idno type="URI">http://authority.nzetc.org/463/</idno>
<idno type="LT">Thomason Tract E.537(17)</idno>
<idno type="Wing">C695</idno>
<idno type="oldCat">
    <g ref="#sym"/>345</idno>
```

## Content Model

```xml
<content>
  <alternate minOccurs="0" maxOccurs="unbounded">
    <textNode/>
    <classRef key="model.gLike"/>
    <elementRef key="idno"/>
  </alternate>
</content>
```
