# `<figDesc>` Beschreibung einer Abbildung

enthält einen kurzen Beschreibungstext des Inhalts oder des Aussehens einer Abbildung, um etwa
    ein Bild ohne dessen Anzeige dokumentieren zu können.

Dieses Element ist als Ersatz für den Inhalt seines Elternelements figure gedacht. Zum
      Beispiel wenn das Bild nicht angezeigt werden kann und man auf einen Alternativtext angewiesen
      ist. Es kann weiters für Indexierungen und Dokumentationen benutzt werden.

Siehe [Textstruktur > Bilder](https://dokumentation.karl-barth.ch/textstruktur/bilder/)

[TEI Guidelines: figDesc](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-figDesc.html)

**Modul:** figures — Abbildungen und Tabellen

## Enthalten in

**figures:** [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik ("

## Kann enthalten

Beliebiger Textinhalt

**core:** [abbr](abbr.md) "Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref" [address](address.md) "enthält eine Postadresse, z. B. eines Verlegers, einer Organ" [bibl](bibl.md) "Bibliographische Angabe. Unterscheidet zwischen gedruckter G" [choice](choice.md) "Gruppiert sic/corr-Paare für Korrekturen der Druckausgabe." [cit](cit.md) "Zitat mit optionaler bibliographischer Angabe." [date](date.md) "Datumsangabe mit maschinenlesbarem Datum in @when, @from/@to" [foreign](foreign.md) "Fremdsprachiger Text. Das @xml:lang gibt die Sprache an, @re" [hi](hi.md) "Hervorhebung. Das @rend gibt die Art an (italic, bold, sup, " [list](list.md) "Liste. Der @type unterscheidet geordnete und ungeordnete Lis" [listBibl](listBibl.md) "enthält eine Liste von bibliografischen Angaben jeglicher Ar" [ptr](ptr.md) "defines a pointer to another location." [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L" [rs](rs.md) "Referenzierende Zeichenkette für Akteure, die nicht als pers" [stage](stage.md) "enthält jegliche Regieanweisung in einem Dramentext oder -fr" [term](term.md) "Sachbegriff mit Verweis auf die Begriffs-Taxonomie via @ref " [title](title.md) "Titel mit verschiedenen Funktionen, unterschieden durch @typ"

**header:** [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer."

**namesdates:** [listEvent](listEvent.md) "contains a list of descriptions, each of which provides info" [orgName](orgName.md) "Name einer Organisation mit Verweis auf die Meta-DB via @ref" [persName](persName.md) "Personenname mit Verweis auf die Meta-DB via @ref (kbga-acto" [placeName](placeName.md) "Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-I"

**figures:** [table](table.md) "Tabelle."

## Content Model

```xml
<content>
    <macroRef key="macro.limitedContent"/>
  </content>
```
