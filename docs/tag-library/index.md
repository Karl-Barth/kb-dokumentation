# Tag-Library

Automatisch generierte Schema-Referenz aus dem TEI ODD der Karl Barth-Gesamtausgabe.

## Textstruktur

[`<TEI>`](TEI.md)
:   enthält ein einzelnes TEI-konformes Dokument, das aus einem einzigen TEI-Header und einem oder
    m

[`<argument>`](argument.md)
:   Zusammenfassung oder Regest eines Textes, typisch am Anfang eines Briefes oder Vortrags.

[`<body>`](body.md)
:   Enthält den gesamten Textkörper eines KBGA-Dokuments.

[`<closer>`](closer.md)
:   Schlussformel eines Briefes (Gruss, Unterschrift, Datum).

[`<dateline>`](dateline.md)
:   enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw. eines Briefs, Zeitungsartikels oder
   

[`<div>`](div.md)
:   Gliederungseinheit eines Textes. Der @type unterscheidet Textsorten (letter, sermon, speech etc.) un

[`<docDate>`](docDate.md)
:   enthält die Datierung des Dokuments, wie auf der Titelseite oder in einer Datumszeile angegeben.

[`<epigraph>`](epigraph.md)
:   enthält ein anonymes oder jemandem zugeschriebenes Zitat, das am Beginn eines Abschnitts,
    Kapite

[`<opener>`](opener.md)
:   fasst Datumszeile, Verfasserangabe, Anredeformel und ähnliche Phrasen zusammen, die einleitend zu
  

[`<postscript>`](postscript.md)
:   enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief.

[`<salute>`](salute.md)
:   enthält eine Anrede oder Grußformel, die einem Vorwort, einer Widmung oder einem anderen
    Abschni

[`<signed>`](signed.md)
:   enthält die abschließende Grußformel o.Ä. die ein Vorwort, eine Widmung oder einen anderen Abschnitt

[`<text>`](text.md)
:   enthält einen einzelnen, eigenständigen oder kompilierten Text, zum Beispiel ein Gedicht oder
    Dr

## Kernmodule

[`<abbr>`](abbr.md)
:   Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref.

[`<addrLine>`](addrLine.md)
:   enthält eine Zeile einer Postadresse.

[`<address>`](address.md)
:   enthält eine Postadresse, z. B. eines Verlegers, einer Organisation oder einer Einzelperson.

[`<author>`](author.md)
:   Verfasserangabe im teiHeader. Das @ref verweist auf die Personen-ID in der Meta-DB.

[`<bibl>`](bibl.md)
:   Bibliographische Angabe. Unterscheidet zwischen gedruckter Gesamtausgabe (pga), Alexander Street Pre

[`<biblScope>`](biblScope.md)
:   Umfangsangabe innerhalb einer bibliographischen Referenz (Seiten, Teilnummer).

[`<choice>`](choice.md)
:   Gruppiert sic/corr-Paare für Korrekturen der Druckausgabe.

[`<cit>`](cit.md)
:   Zitat mit optionaler bibliographischer Angabe.

[`<corr>`](corr.md)
:   Korrektur eines Fehlers in der Druckausgabe. Der @type unterscheidet inhaltliche Korrekturen (corr),

[`<date>`](date.md)
:   enthält ein Datum in beliebigem Format.

[`<editor>`](editor.md)
:   Herausgeberangabe in einer bibliographischen Referenz.

[`<foreign>`](foreign.md)
:   identifiziert ein Wort oder eine Phrase, die zu einer anderen Sprache gehört, als der umgebende Text

[`<graphic>`](graphic.md)
:   gibt den Ort einer Bildressource an, 
    die entweder Teil eines Texts oder ein Abbild dessen ist.

[`<head>`](head.md)
:   Überschrift einer Gliederungseinheit (div).

[`<hi>`](hi.md)
:   markiert ein Wort oder eine Textpassage, das/die sich grafisch vom umgebenden Text abhebt, ohne dass

[`<item>`](item.md)
:   enthält einen Listenpunkt.

[`<l>`](l.md)
:   enthält eine einzelne, möglicherweise unvollständige, Verszeile.

[`<lb>`](lb.md)
:   markiert den Anfang einer neuen typographischen 
    Zeile in einer bestimmten Auflage oder Version 

[`<lg>`](lg.md)
:   enthält eine oder mehrere Verse bzw. Verszeilen, die zusammen eine formale Einheit (z. B. Strophe, R

[`<list>`](list.md)
:   enthält eine Reihe von Listenpunkten, die als Liste organisiert sind.

[`<listBibl>`](listBibl.md)
:   enthält eine Liste von bibliografischen Angaben jeglicher Art.

[`<milestone>`](milestone.md)
:   markiert einen Grenzpunkt, der Abschnitte eines Textes trennen kann, 
    typischerweise (aber nicht

[`<note>`](note.md)
:   enthält eine Anmerkung oder Annotation.

[`<p>`](p.md)
:   Absatz. Darf nicht verschachtelt werden (ausser innerhalb von note).

[`<pb>`](pb.md)
:   Seitenumbruch. Das @ed unterscheidet die Ausgabe (pga, A), @n die Seitenzahl.

[`<ptr>`](ptr.md)
:   defines a pointer to another location.

[`<pubPlace>`](pubPlace.md)
:   enthält den Namen des Orts, an dem ein bibliografisches Objekt veröffentlicht wurde.

[`<publisher>`](publisher.md)
:   gibt den Namen der Organisation an, die für die Veröffentlichung und Verbreitung eines
    bibliogra

[`<q>`](q.md)
:   enthält Material, das vom umgebenden Text durch 
    Anführungszeichen oder ähnliche Methoden abgese

[`<quote>`](quote.md)
:   Zitat innerhalb des Textes.

[`<ref>`](ref.md)
:   Verweis auf eine andere Ressource. Dient für Bibelstellen, Literaturverweise, Querverweise und URLs.

[`<rs>`](rs.md)
:   Referenzierende Zeichenkette für Akteure, die nicht als persName oder orgName ausgezeichnet werden (

[`<sic>`](sic.md)
:   Markiert die fehlerhafte Stelle in der Druckausgabe (innerhalb von choice/sic/corr). Das @ed gibt di

[`<sp>`](sp.md)
:   enthält eine einzelne Figurenrede in einem Dramentext oder eine entsprechende Passage in einem Prosa

[`<speaker>`](speaker.md)
:   enthält eine spezielle Form von Überschrift oder Bezeichnung für einen oder mehrere Namen von
    Fi

[`<stage>`](stage.md)
:   enthält jegliche Regieanweisung in einem Dramentext oder -fragment.

[`<term>`](term.md)
:   enthält ein einzelnes Wort, Mehrworttermini 
        oder symbolische Bezeichnungen, die als Fachbeg

[`<title>`](title.md)
:   Titel mit verschiedenen Funktionen, unterschieden durch @type: Bandtitel (volume), inhaltlicher Tite

## Header

[`<availability>`](availability.md)
:   Lizenzinformationen zur Publikation. Wird aus der Datenbank generiert.

[`<change>`](change.md)
:   Änderungsvermerk in der revisionDesc. Enthält Zeitstempel der letzten Header-Generierung.

[`<correspAction>`](correspAction.md)
:   contains a structured
  description of the place, the name of a person/organization and the
  date r

[`<correspContext>`](correspContext.md)
:   provides references to preceding or following correspondence related to this piece of correspondence

[`<correspDesc>`](correspDesc.md)
:   contains a description
    of the actions related to one act of correspondence.

[`<creation>`](creation.md)
:   beinhaltet Informationen zur Entstehung eines Textes.

[`<edition>`](edition.md)
:   beschreibt die Details einer Ausgabe eines Textes.

[`<editionStmt>`](editionStmt.md)
:   Angaben zur digitalen Edition (Titel, Förderer).

[`<encodingDesc>`](encodingDesc.md)
:   dokumentiert das Verhältnis zwischen dem elektronischen Text und seiner Quelle oder den Quellen, von

[`<fileDesc>`](fileDesc.md)
:   enthält die vollständige bibliografische Beschreibung einer elektronischen Datei.

[`<idno>`](idno.md)
:   Identifikator, z.B. URL oder KBA-Objektnummer.

[`<keywords>`](keywords.md)
:   enthält eine Zusammenstellung von Schlagwörtern oder Phrasen zur Art oder Thematik des Textes.

[`<langUsage>`](langUsage.md)
:   beschreibt Sprachen, Subsprachen, Register, Dialekte usw., die innerhalb eines Textes vorkommen.

[`<language>`](language.md)
:   beschreibt eine einzelne Sprache oder eine Subsprache, die innerhalb eines Textes verwendet wird.

[`<licence>`](licence.md)
:   beinhaltet für den Text gültige Lizenzinformationen oder andere rechtswirksame Vereinbarungen.

[`<listPrefixDef>`](listPrefixDef.md)
:   contains a list of definitions of prefixing schemes used in teidata.pointer values, showing how abbr

[`<prefixDef>`](prefixDef.md)
:   defines a prefixing scheme used in teidata.pointer values,
  showing how abbreviated URIs using the 

[`<profileDesc>`](profileDesc.md)
:   enthält eine detaillierte Beschreibung der nicht-bibliografischen Merkmale des Textes, besonders der

[`<publicationStmt>`](publicationStmt.md)
:   umfasst Angaben zu Veröffentlichung oder Vertrieb eines elektronischen oder sonstigen Textes.

[`<revisionDesc>`](revisionDesc.md)
:   dokumentiert die Änderungen, die an der Datei vorgenommen wurden.

[`<sourceDesc>`](sourceDesc.md)
:   beschreibt die Quelle, von der sich der elektronische Text ableitet. 
        Üblicherweise eine bib

[`<sponsor>`](sponsor.md)
:   gibt den Namen einer Organisation oder Institution an, die als Förderer auftritt.

[`<teiHeader>`](teiHeader.md)
:   wird aus der Meta- und Registerdatenbank erzeugt und soll im XML nicht verändert werden (https://met

[`<textClass>`](textClass.md)
:   gruppiert Informationen über Art oder Thematik eines Textes unter 
      Bezug auf ein Standard-Klas

[`<titleStmt>`](titleStmt.md)
:   sollte mehrere Titel für verschiedene Zwecke enhalten.

## Linking

[`<ab>`](ab.md)
:   Anonymer Block, verwendet für zentrierte oder anders formatierte Textabschnitte ohne Absatz-Semantik

[`<anchor>`](anchor.md)
:   Ankerpunkt für Querverweise (@type='cross') und für Fussnoten mit mehreren Fussnotenzeichen (@type='

[`<seg>`](seg.md)
:   beschreibt Segmente eines Texts unterhalb des Chunk-Level.

## Namen und Daten

[`<event>`](event.md)
:   enthält Daten mit Bezug zu etwas Bemerkenswertem, das in der Zeit geschieht.

[`<listEvent>`](listEvent.md)
:   contains a list of descriptions, each of which provides information about an identifiable event.

[`<orgName>`](orgName.md)
:   Name einer Organisation mit Verweis auf die Meta-DB via @ref.

[`<persName>`](persName.md)
:   Personenname mit Verweis auf die Meta-DB via @ref (kbga-actors-ID). Das @key kann provisorisch eine 

[`<placeName>`](placeName.md)
:   Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-ID). Das @key kann provisorisch eine norm

## Abbildungen und Tabellen

[`<cell>`](cell.md)
:   Tabellenzelle.

[`<figDesc>`](figDesc.md)
:   enthält einen kurzen Beschreibungstext des Inhalts oder des Aussehens einer Abbildung, um etwa
    e

[`<figure>`](figure.md)
:   Abbildung mit optionaler Beschreibung (figDesc) und Grafik (graphic).

[`<row>`](row.md)
:   enthält eine Zeile einer Tabelle.

[`<table>`](table.md)
:   enthält Text, der in Tabellenform, also in Zeilen und Spalten, dargestellt ist.

## Handschriftenbeschreibung

[`<altIdentifier>`](altIdentifier.md)
:   Alternativer Identifikator für eine Quelle (URI, KBA-ID, KBGA-Sources-ID).

[`<msContents>`](msContents.md)
:   describes the intellectual content of a manuscript, manuscript
    part, or other object either as a

[`<msDesc>`](msDesc.md)
:   contains a description of a single identifiable
    manuscript or other text-bearing object such as 

[`<msIdentifier>`](msIdentifier.md)
:   contains the information required to identify the manuscript or similar object being described.

[`<msItem>`](msItem.md)
:   describes an individual work or item within the intellectual
  content of a manuscript, manuscript p

[`<repository>`](repository.md)
:   contains the name of a repository within which manuscripts or other objects are stored, possibly for

## Transkription

[`<metamark>`](metamark.md)
:   contains or describes any kind of graphic or written signal
   within a document the function of whi

## Analyse

[`<span>`](span.md)
:   associates an interpretative annotation directly with a span of text.
