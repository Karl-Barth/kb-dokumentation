# `<author>` Autor

Verfasserangabe im teiHeader. Das @ref verweist auf die Personen-ID in der Meta-DB.

Insbesondere wenn eine Katalogisierung auf Basis des TEI-Headers erfolgen soll, ist es ratsam
      einen Namen aus einer annerkannten Normdatei zu verwenden. Die Attribute key und
      ref können außerdem benutzt werden, um auf kanonische Informationen über
      einen Autor zu verweisen, etwa in einem Bibliothekskatalog oder einer Online-Ressource.
    Im Fall von Rundfunksendungen sollte dies Element benutzt werden, um den Namen der Firma oder
      der Sendergruppe zu notieren, welche diese Rundfunksendung verantwortet.
    Wo ein Autor unbekannt oder nicht angegeben ist, kann dieses Element Text wie z. B.
      Unbekannt oder Nicht angegeben beinhalten.
      Wenn die entsprechenden TEI-Module benutzt werden, kann das Element auch detaillierte
      Auszeichnungen für Namen von Personen, Organisationen oder Orten beinhalten - insbesondere
      wenn mehrere Namen vorhanden sind.

[TEI Guidelines: author](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-author.html)

**Modul:** core — Kernmodule

## Attribute

**@ref** (optional)
:   Datentyp: teidata.pattern


## Enthalten in

**core:** [bibl](bibl.md) "Bibliographische Angabe. Unterscheidet zwischen gedruckter G"

**header:** [editionStmt](editionStmt.md) "Angaben zur digitalen Edition (Titel, Förderer)." [titleStmt](titleStmt.md) "sollte mehrere Titel für verschiedene Zwecke enhalten."

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
