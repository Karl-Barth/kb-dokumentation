# Tag-Library

Schema-Referenz der Karl Barth-Gesamtausgabe, generiert aus dem TEI ODD.

## Dokumentstruktur

[TEI](TEI.md)
:   enthält ein einzelnes TEI-konformes Dokument, das aus einem einzigen TEI-Header und einem oder
    mehreren Mitgliedern 

[text](text.md)
:   enthält einen einzelnen, eigenständigen oder kompilierten Text, zum Beispiel ein Gedicht oder
    Drama, eine Sammlung v

[body](body.md)
:   Enthält den gesamten Textkörper eines KBGA-Dokuments.

[teiHeader](teiHeader.md)
:   wird aus der Meta- und Registerdatenbank erzeugt und soll im XML nicht verändert werden (https://meta.karl-barth.ch)


## Elemente im Textbereich

### Textstruktur

[div](div.md)
:   Gliederungseinheit eines Textes. Der @type unterscheidet Textsorten (letter, sermon, speech etc.) und Strukturteile (ope

[p](p.md)
:   Absatz. Darf nicht verschachtelt werden (ausser innerhalb von note).

[ab](ab.md)
:   Anonymer Block, verwendet für zentrierte oder anders formatierte Textabschnitte ohne Absatz-Semantik.

[head](head.md)
:   Überschrift einer Gliederungseinheit (div).

[opener](opener.md)
:   fasst Datumszeile, Verfasserangabe, Anredeformel und ähnliche Phrasen zusammen, die einleitend zu
    Beginn eines Absch

[closer](closer.md)
:   Schlussformel eines Briefes (Gruss, Unterschrift, Datum).

[dateline](dateline.md)
:   enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw. eines Briefs, Zeitungsartikels oder
    anderen Werks. Dies

[salute](salute.md)
:   enthält eine Anrede oder Grußformel, die einem Vorwort, einer Widmung oder einem anderen
    Abschnitt eines Textes vora

[signed](signed.md)
:   enthält die abschließende Grußformel o.Ä. die ein Vorwort, eine Widmung oder einen anderen Abschnitt des Textes beendet.

[postscript](postscript.md)
:   enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief.

[epigraph](epigraph.md)
:   enthält ein anonymes oder jemandem zugeschriebenes Zitat, das am Beginn eines Abschnitts,
    Kapitels oder auf einer Ti

[argument](argument.md)
:   Zusammenfassung oder Regest eines Textes, typisch am Anfang eines Briefes oder Vortrags.


### Querverweise und Verknüpfungen

[ref](ref.md)
:   Verweis auf eine andere Ressource. Dient für Bibelstellen, Literaturverweise, Querverweise und URLs.

[ptr](ptr.md)
:   defines a pointer to another location.

[anchor](anchor.md)
:   Ankerpunkt für Querverweise (@type='cross') und für Fussnoten mit mehreren Fussnotenzeichen (@type='note').

[seg](seg.md)
:   Segment. Verwendet für nicht-Entitäten, Verse, Biogramme, Hervorhebungen und Übersetzungen.

[milestone](milestone.md)
:   markiert einen Grenzpunkt, der Abschnitte eines Textes trennen kann, 
    typischerweise (aber nicht notwendigerweise) d


### Listen und Tabellen

[list](list.md)
:   Liste. Der @type unterscheidet geordnete und ungeordnete Listen.

[item](item.md)
:   enthält einen Listenpunkt.

[table](table.md)
:   Tabelle.

[row](row.md)
:   enthält eine Zeile einer Tabelle.

[cell](cell.md)
:   Tabellenzelle.


### Gedichte und wörtliche Rede

[lg](lg.md)
:   Strophe oder Versgruppe.

[l](l.md)
:   Verszeile.

[q](q.md)
:   Direkte Rede oder Zitat im Fliesstext.

[quote](quote.md)
:   Zitat innerhalb des Textes.

[cit](cit.md)
:   Zitat mit optionaler bibliographischer Angabe.

[sp](sp.md)
:   enthält eine einzelne Figurenrede in einem Dramentext oder eine entsprechende Passage in einem Prosatext oder lyrischen 

[speaker](speaker.md)
:   enthält eine spezielle Form von Überschrift oder Bezeichnung für einen oder mehrere Namen von
    Figuren in einem Drame

[stage](stage.md)
:   enthält jegliche Regieanweisung in einem Dramentext oder -fragment.


### Typographie und Korrekturen

[hi](hi.md)
:   Hervorhebung. Das @rend gibt die Art an (italic, bold, sup, sub etc.).

[foreign](foreign.md)
:   Fremdsprachiger Text. Das @xml:lang gibt die Sprache an, @rend das Darstellungsformat (z.B. Ell für Griechisch).

[lb](lb.md)
:   markiert den Anfang einer neuen typographischen 
    Zeile in einer bestimmten Auflage oder Version eines Textes.

[pb](pb.md)
:   Seitenumbruch. Das @ed unterscheidet die Ausgabe (pga, A), @n die Seitenzahl.

[choice](choice.md)
:   Gruppiert sic/corr-Paare für Korrekturen der Druckausgabe.

[sic](sic.md)
:   Markiert die fehlerhafte Stelle in der Druckausgabe (innerhalb von choice/sic/corr). Das @ed gibt die Ausgabe an (typisc

[corr](corr.md)
:   Korrektur eines Fehlers in der Druckausgabe. Der @type unterscheidet inhaltliche Korrekturen (corr), Druckfehler (mispri

[abbr](abbr.md)
:   Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref.


### Abbildungen

[figure](figure.md)
:   Abbildung mit optionaler Beschreibung (figDesc) und Grafik (graphic).

[graphic](graphic.md)
:   Verweis auf eine Bilddatei via @url.

[figDesc](figDesc.md)
:   enthält einen kurzen Beschreibungstext des Inhalts oder des Aussehens einer Abbildung, um etwa
    ein Bild ohne dessen 


### Semantische Auszeichnung

[persName](persName.md)
:   Personenname mit Verweis auf die Meta-DB via @ref (kbga-actors-ID). Das @key kann provisorisch eine normalisierte Schrei

[orgName](orgName.md)
:   Name einer Organisation mit Verweis auf die Meta-DB via @ref.

[placeName](placeName.md)
:   Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-ID). Das @key kann provisorisch eine normalisierte Schreibwei

[rs](rs.md)
:   Referenzierende Zeichenkette für Akteure, die nicht als persName oder orgName ausgezeichnet werden (z.B. Pronomen, Umsch

[date](date.md)
:   Datumsangabe mit maschinenlesbarem Datum in @when, @from/@to oder @notBefore/@notAfter.

[term](term.md)
:   Sachbegriff mit Verweis auf die Begriffs-Taxonomie via @ref oder @key.

[bibl](bibl.md)
:   Bibliographische Angabe. Unterscheidet zwischen gedruckter Gesamtausgabe (pga), Alexander Street Press (asp), Quellen (s

[biblScope](biblScope.md)
:   Umfangsangabe innerhalb einer bibliographischen Referenz (Seiten, Teilnummer).

[listBibl](listBibl.md)
:   enthält eine Liste von bibliografischen Angaben jeglicher Art.

[note](note.md)
:   Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @type unterscheidet Fussnoten und editorische Anmerkungen.


### Weitere Textelemente

[address](address.md)
:   enthält eine Postadresse, z. B. eines Verlegers, einer Organisation oder einer Einzelperson.

[addrLine](addrLine.md)
:   enthält eine Zeile einer Postadresse.

[author](author.md)
:   Verfasserangabe im teiHeader. Das @ref verweist auf die Personen-ID in der Meta-DB.

[editor](editor.md)
:   Herausgeberangabe in einer bibliographischen Referenz.

[docDate](docDate.md)
:   enthält die Datierung des Dokuments, wie auf der Titelseite oder in einer Datumszeile angegeben.

[metamark](metamark.md)
:   contains or describes any kind of graphic or written signal
   within a document the function of which is to determine h

[span](span.md)
:   associates an interpretative annotation directly with a span of text.


## Elemente im Kopfbereich

### Dateibeschreibung

[fileDesc](fileDesc.md)
:   enthält die vollständige bibliografische Beschreibung einer elektronischen Datei.

[titleStmt](titleStmt.md)
:   sollte mehrere Titel für verschiedene Zwecke enhalten.

[title](title.md)
:   Titel mit verschiedenen Funktionen, unterschieden durch @type: Bandtitel (volume), inhaltlicher Titel (content), formale

[editionStmt](editionStmt.md)
:   Angaben zur digitalen Edition (Titel, Förderer).

[edition](edition.md)
:   beschreibt die Details einer Ausgabe eines Textes.

[publicationStmt](publicationStmt.md)
:   umfasst Angaben zu Veröffentlichung oder Vertrieb eines elektronischen oder sonstigen Textes.

[publisher](publisher.md)
:   gibt den Namen der Organisation an, die für die Veröffentlichung und Verbreitung eines
    bibliografischen Objekts vera

[pubPlace](pubPlace.md)
:   enthält den Namen des Orts, an dem ein bibliografisches Objekt veröffentlicht wurde.

[availability](availability.md)
:   Lizenzinformationen zur Publikation. Wird aus der Datenbank generiert.

[licence](licence.md)
:   beinhaltet für den Text gültige Lizenzinformationen oder andere rechtswirksame Vereinbarungen.

[sourceDesc](sourceDesc.md)
:   beschreibt die Quelle, von der sich der elektronische Text ableitet. 
        Üblicherweise eine bibliografische Beschre

[idno](idno.md)
:   Identifikator, z.B. URL oder KBA-Objektnummer.


### Quellenbeschreibung

[msDesc](msDesc.md)
:   contains a description of a single identifiable
    manuscript or other text-bearing object such as an early printed boo

[msIdentifier](msIdentifier.md)
:   contains the information required to identify the manuscript or similar object being described.

[repository](repository.md)
:   contains the name of a repository within which manuscripts or other objects are stored, possibly forming part of an inst

[altIdentifier](altIdentifier.md)
:   Alternativer Identifikator für eine Quelle (URI, KBA-ID, KBGA-Sources-ID).

[msContents](msContents.md)
:   describes the intellectual content of a manuscript, manuscript
    part, or other object either as a series of paragraph

[msItem](msItem.md)
:   describes an individual work or item within the intellectual
  content of a manuscript, manuscript part, or other object


### Kodierungsbeschreibung

[encodingDesc](encodingDesc.md)
:   dokumentiert das Verhältnis zwischen dem elektronischen Text und seiner Quelle oder den Quellen, von denen er sich ablei

[listPrefixDef](listPrefixDef.md)
:   contains a list of definitions of prefixing schemes used in teidata.pointer values, showing how abbreviated URIs using e

[prefixDef](prefixDef.md)
:   defines a prefixing scheme used in teidata.pointer values,
  showing how abbreviated URIs using the scheme may be expand


### Textprofil

[profileDesc](profileDesc.md)
:   enthält eine detaillierte Beschreibung der nicht-bibliografischen Merkmale des Textes, besonders der verwendeten Sprache

[creation](creation.md)
:   beinhaltet Informationen zur Entstehung eines Textes.

[langUsage](langUsage.md)
:   beschreibt Sprachen, Subsprachen, Register, Dialekte usw., die innerhalb eines Textes vorkommen.

[language](language.md)
:   beschreibt eine einzelne Sprache oder eine Subsprache, die innerhalb eines Textes verwendet wird.

[textClass](textClass.md)
:   gruppiert Informationen über Art oder Thematik eines Textes unter 
      Bezug auf ein Standard-Klassifikationsschema, e

[keywords](keywords.md)
:   enthält eine Zusammenstellung von Schlagwörtern oder Phrasen zur Art oder Thematik des Textes.


### Korrespondenzbeschreibung

[correspDesc](correspDesc.md)
:   contains a description
    of the actions related to one act of correspondence.

[correspAction](correspAction.md)
:   contains a structured
  description of the place, the name of a person/organization and the
  date related to the sendin

[correspContext](correspContext.md)
:   provides references to preceding or following correspondence related to this piece of correspondence.


### Weitere Header-Elemente

[sponsor](sponsor.md)
:   gibt den Namen einer Organisation oder Institution an, die als Förderer auftritt.

[change](change.md)
:   Änderungsvermerk in der revisionDesc. Enthält Zeitstempel der letzten Header-Generierung.

[revisionDesc](revisionDesc.md)
:   dokumentiert die Änderungen, die an der Datei vorgenommen wurden.

[event](event.md)
:   enthält Daten mit Bezug zu etwas Bemerkenswertem, das in der Zeit geschieht.

[listEvent](listEvent.md)
:   contains a list of descriptions, each of which provides information about an identifiable event.

