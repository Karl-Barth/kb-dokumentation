# Tag-Library

Automatisch generierte Schema-Referenz aus dem TEI ODD der Karl Barth-Gesamtausgabe.

| Element | Modul | Beschreibung |
|---------|-------|-------------|
| [`<TEI>`](TEI.md) | textstructure | enthält ein einzelnes TEI-konformes Dokument, das aus einem einzigen TEI-Header  |
| [`<ab>`](ab.md) | linking | Anonymer Block, verwendet für zentrierte oder anders formatierte Textabschnitte  |
| [`<abbr>`](abbr.md) | core | Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref. |
| [`<addrLine>`](addrLine.md) | core | enthält eine Zeile einer Postadresse. |
| [`<address>`](address.md) | core | enthält eine Postadresse, z. B. eines Verlegers, einer Organisation oder einer E |
| [`<altIdentifier>`](altIdentifier.md) | msdescription | Alternativer Identifikator für eine Quelle (URI, KBA-ID, KBGA-Sources-ID). |
| [`<anchor>`](anchor.md) | linking | Ankerpunkt für Querverweise (@type='cross') und für Fussnoten mit mehreren Fussn |
| [`<argument>`](argument.md) | textstructure | Zusammenfassung oder Regest eines Textes, typisch am Anfang eines Briefes oder V |
| [`<author>`](author.md) | core | Verfasserangabe im teiHeader. Das @ref verweist auf die Personen-ID in der Meta- |
| [`<availability>`](availability.md) | header | Lizenzinformationen zur Publikation. Wird aus der Datenbank generiert. |
| [`<bibl>`](bibl.md) | core | Bibliographische Angabe. Unterscheidet zwischen gedruckter Gesamtausgabe (pga),  |
| [`<biblScope>`](biblScope.md) | core | Umfangsangabe innerhalb einer bibliographischen Referenz (Seiten, Teilnummer). |
| [`<body>`](body.md) | textstructure | Enthält den gesamten Textkörper eines KBGA-Dokuments. |
| [`<cell>`](cell.md) | figures | Tabellenzelle. |
| [`<change>`](change.md) | header | Änderungsvermerk in der revisionDesc. Enthält Zeitstempel der letzten Header-Gen |
| [`<choice>`](choice.md) | core | Gruppiert sic/corr-Paare für Korrekturen der Druckausgabe. |
| [`<cit>`](cit.md) | core | Zitat mit optionaler bibliographischer Angabe. |
| [`<closer>`](closer.md) | textstructure | Schlussformel eines Briefes (Gruss, Unterschrift, Datum). |
| [`<corr>`](corr.md) | core | Korrektur eines Fehlers in der Druckausgabe. Der @type unterscheidet inhaltliche |
| [`<correspAction>`](correspAction.md) | header | contains a structured
  description of the place, the name of a person/organizat |
| [`<correspContext>`](correspContext.md) | header | provides references to preceding or following correspondence related to this pie |
| [`<correspDesc>`](correspDesc.md) | header | contains a description
    of the actions related to one act of correspondence. |
| [`<creation>`](creation.md) | header | beinhaltet Informationen zur Entstehung eines Textes. |
| [`<date>`](date.md) | core | enthält ein Datum in beliebigem Format. |
| [`<dateline>`](dateline.md) | textstructure | enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw. eines Briefs, Zeitu |
| [`<div>`](div.md) | textstructure | Gliederungseinheit eines Textes. Der @type unterscheidet Textsorten (letter, ser |
| [`<docDate>`](docDate.md) | textstructure | enthält die Datierung des Dokuments, wie auf der Titelseite oder in einer Datums |
| [`<edition>`](edition.md) | header | beschreibt die Details einer Ausgabe eines Textes. |
| [`<editionStmt>`](editionStmt.md) | header | Angaben zur digitalen Edition (Titel, Förderer). |
| [`<editor>`](editor.md) | core | Herausgeberangabe in einer bibliographischen Referenz. |
| [`<encodingDesc>`](encodingDesc.md) | header | dokumentiert das Verhältnis zwischen dem elektronischen Text und seiner Quelle o |
| [`<epigraph>`](epigraph.md) | textstructure | enthält ein anonymes oder jemandem zugeschriebenes Zitat, das am Beginn eines Ab |
| [`<event>`](event.md) | namesdates | enthält Daten mit Bezug zu etwas Bemerkenswertem, das in der Zeit geschieht. |
| [`<figDesc>`](figDesc.md) | figures | enthält einen kurzen Beschreibungstext des Inhalts oder des Aussehens einer Abbi |
| [`<figure>`](figure.md) | figures | Abbildung mit optionaler Beschreibung (figDesc) und Grafik (graphic). |
| [`<fileDesc>`](fileDesc.md) | header | enthält die vollständige bibliografische Beschreibung einer elektronischen Datei |
| [`<foreign>`](foreign.md) | core | identifiziert ein Wort oder eine Phrase, die zu einer anderen Sprache gehört, al |
| [`<graphic>`](graphic.md) | core | gibt den Ort einer Bildressource an, 
    die entweder Teil eines Texts oder ein |
| [`<head>`](head.md) | core | Überschrift einer Gliederungseinheit (div). |
| [`<hi>`](hi.md) | core | markiert ein Wort oder eine Textpassage, das/die sich grafisch vom umgebenden Te |
| [`<idno>`](idno.md) | header | Identifikator, z.B. URL oder KBA-Objektnummer. |
| [`<item>`](item.md) | core | enthält einen Listenpunkt. |
| [`<keywords>`](keywords.md) | header | enthält eine Zusammenstellung von Schlagwörtern oder Phrasen zur Art oder Themat |
| [`<l>`](l.md) | core | enthält eine einzelne, möglicherweise unvollständige, Verszeile. |
| [`<langUsage>`](langUsage.md) | header | beschreibt Sprachen, Subsprachen, Register, Dialekte usw., die innerhalb eines T |
| [`<language>`](language.md) | header | beschreibt eine einzelne Sprache oder eine Subsprache, die innerhalb eines Texte |
| [`<lb>`](lb.md) | core | markiert den Anfang einer neuen typographischen 
    Zeile in einer bestimmten A |
| [`<lg>`](lg.md) | core | enthält eine oder mehrere Verse bzw. Verszeilen, die zusammen eine formale Einhe |
| [`<licence>`](licence.md) | header | beinhaltet für den Text gültige Lizenzinformationen oder andere rechtswirksame V |
| [`<list>`](list.md) | core | enthält eine Reihe von Listenpunkten, die als Liste organisiert sind. |
| [`<listBibl>`](listBibl.md) | core | enthält eine Liste von bibliografischen Angaben jeglicher Art. |
| [`<listEvent>`](listEvent.md) | namesdates | contains a list of descriptions, each of which provides information about an ide |
| [`<listPrefixDef>`](listPrefixDef.md) | header | contains a list of definitions of prefixing schemes used in teidata.pointer valu |
| [`<metamark>`](metamark.md) | transcr | contains or describes any kind of graphic or written signal
   within a document |
| [`<milestone>`](milestone.md) | core | markiert einen Grenzpunkt, der Abschnitte eines Textes trennen kann, 
    typisc |
| [`<msContents>`](msContents.md) | msdescription | describes the intellectual content of a manuscript, manuscript
    part, or othe |
| [`<msDesc>`](msDesc.md) | msdescription | contains a description of a single identifiable
    manuscript or other text-bea |
| [`<msIdentifier>`](msIdentifier.md) | msdescription | contains the information required to identify the manuscript or similar object b |
| [`<msItem>`](msItem.md) | msdescription | describes an individual work or item within the intellectual
  content of a manu |
| [`<note>`](note.md) | core | enthält eine Anmerkung oder Annotation. |
| [`<opener>`](opener.md) | textstructure | fasst Datumszeile, Verfasserangabe, Anredeformel und ähnliche Phrasen zusammen,  |
| [`<orgName>`](orgName.md) | namesdates | Name einer Organisation mit Verweis auf die Meta-DB via @ref. |
| [`<p>`](p.md) | core | Absatz. Darf nicht verschachtelt werden (ausser innerhalb von note). |
| [`<pb>`](pb.md) | core | Seitenumbruch. Das @ed unterscheidet die Ausgabe (pga, A), @n die Seitenzahl. |
| [`<persName>`](persName.md) | namesdates | Personenname mit Verweis auf die Meta-DB via @ref (kbga-actors-ID). Das @key kan |
| [`<placeName>`](placeName.md) | namesdates | Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-ID). Das @key kann pr |
| [`<postscript>`](postscript.md) | textstructure | enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief. |
| [`<prefixDef>`](prefixDef.md) | header | defines a prefixing scheme used in teidata.pointer values,
  showing how abbrevi |
| [`<profileDesc>`](profileDesc.md) | header | enthält eine detaillierte Beschreibung der nicht-bibliografischen Merkmale des T |
| [`<ptr>`](ptr.md) | core | defines a pointer to another location. |
| [`<pubPlace>`](pubPlace.md) | core | enthält den Namen des Orts, an dem ein bibliografisches Objekt veröffentlicht wu |
| [`<publicationStmt>`](publicationStmt.md) | header | umfasst Angaben zu Veröffentlichung oder Vertrieb eines elektronischen oder sons |
| [`<publisher>`](publisher.md) | core | gibt den Namen der Organisation an, die für die Veröffentlichung und Verbreitung |
| [`<q>`](q.md) | core | enthält Material, das vom umgebenden Text durch 
    Anführungszeichen oder ähnl |
| [`<quote>`](quote.md) | core | Zitat innerhalb des Textes. |
| [`<ref>`](ref.md) | core | Verweis auf eine andere Ressource. Dient für Bibelstellen, Literaturverweise, Qu |
| [`<repository>`](repository.md) | msdescription | contains the name of a repository within which manuscripts or other objects are  |
| [`<revisionDesc>`](revisionDesc.md) | header | dokumentiert die Änderungen, die an der Datei vorgenommen wurden. |
| [`<row>`](row.md) | figures | enthält eine Zeile einer Tabelle. |
| [`<rs>`](rs.md) | core | Referenzierende Zeichenkette für Akteure, die nicht als persName oder orgName au |
| [`<salute>`](salute.md) | textstructure | enthält eine Anrede oder Grußformel, die einem Vorwort, einer Widmung oder einem |
| [`<seg>`](seg.md) | linking | beschreibt Segmente eines Texts unterhalb des Chunk-Level. |
| [`<sic>`](sic.md) | core | Markiert die fehlerhafte Stelle in der Druckausgabe (innerhalb von choice/sic/co |
| [`<signed>`](signed.md) | textstructure | enthält die abschließende Grußformel o.Ä. die ein Vorwort, eine Widmung oder ein |
| [`<sourceDesc>`](sourceDesc.md) | header | beschreibt die Quelle, von der sich der elektronische Text ableitet. 
        Üb |
| [`<sp>`](sp.md) | core | enthält eine einzelne Figurenrede in einem Dramentext oder eine entsprechende Pa |
| [`<span>`](span.md) | analysis | associates an interpretative annotation directly with a span of text. |
| [`<speaker>`](speaker.md) | core | enthält eine spezielle Form von Überschrift oder Bezeichnung für einen oder mehr |
| [`<sponsor>`](sponsor.md) | header | gibt den Namen einer Organisation oder Institution an, die als Förderer auftritt |
| [`<stage>`](stage.md) | core | enthält jegliche Regieanweisung in einem Dramentext oder -fragment. |
| [`<table>`](table.md) | figures | enthält Text, der in Tabellenform, also in Zeilen und Spalten, dargestellt ist. |
| [`<teiHeader>`](teiHeader.md) | header | wird aus der Meta- und Registerdatenbank erzeugt und soll im XML nicht verändert |
| [`<term>`](term.md) | core | enthält ein einzelnes Wort, Mehrworttermini 
        oder symbolische Bezeichnun |
| [`<text>`](text.md) | textstructure | enthält einen einzelnen, eigenständigen oder kompilierten Text, zum Beispiel ein |
| [`<textClass>`](textClass.md) | header | gruppiert Informationen über Art oder Thematik eines Textes unter 
      Bezug a |
| [`<title>`](title.md) | core | Titel mit verschiedenen Funktionen, unterschieden durch @type: Bandtitel (volume |
| [`<titleStmt>`](titleStmt.md) | header | sollte mehrere Titel für verschiedene Zwecke enhalten. |
