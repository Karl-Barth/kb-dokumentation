# `<sp>` Figurenrede

enthält eine einzelne Figurenrede in einem Dramentext oder eine entsprechende Passage in einem Prosatext oder lyrischen Text.

Das who-Attribut an diesem Element kann entweder zusätzlich zum
      speaker-Element eingesetzt werden oder alternativ dazu.

Siehe [Textstruktur > Woertliche Rede](https://dokumentation.karl-barth.ch/textstruktur/woertliche-rede/)

[TEI Guidelines: sp](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-sp.html)

**Modul:** core — Kernmodule

## Enthalten in

**textstructure:** [argument](argument.md) "Zusammenfassung oder Regest eines Textes, typisch am Anfang " [body](body.md) "Enthält den gesamten Textkörper eines KBGA-Dokuments." [div](div.md) "Gliederungseinheit eines Textes. Der @type unterscheidet Tex" [epigraph](epigraph.md) "enthält ein anonymes oder jemandem zugeschriebenes Zitat, da" [postscript](postscript.md) "enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief."

**core:** [item](item.md) "enthält einen Listenpunkt." [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [stage](stage.md) "enthält jegliche Regieanweisung in einem Dramentext oder -fr"

**header:** [change](change.md) "Änderungsvermerk in der revisionDesc. Enthält Zeitstempel de" [licence](licence.md) "beinhaltet für den Text gültige Lizenzinformationen oder and"

**figures:** [cell](cell.md) "Tabellenzelle." [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik ("

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
"

## Kann enthalten

**core:** [cit](cit.md) "Zitat mit optionaler bibliographischer Angabe." [l](l.md) "Verszeile." [lb](lb.md) "markiert den Anfang einer neuen typographischen 
    Zeile i" [lg](lg.md) "Strophe oder Versgruppe." [list](list.md) "Liste. Der @type unterscheidet geordnete und ungeordnete Lis" [milestone](milestone.md) "markiert einen Grenzpunkt, der Abschnitte eines Textes trenn" [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo" [pb](pb.md) "Seitenumbruch. Das @ed unterscheidet die Ausgabe (pga, A), @" [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [speaker](speaker.md) "enthält eine spezielle Form von Überschrift oder Bezeichnung" [stage](stage.md) "enthält jegliche Regieanweisung in einem Dramentext oder -fr"

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati" [anchor](anchor.md) "Ankerpunkt für Querverweise (@type='cross') und für Fussnote"

**namesdates:** [listEvent](listEvent.md) "contains a list of descriptions, each of which provides info"

**figures:** [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik (" [table](table.md) "Tabelle."

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
"

**analysis:** [span](span.md) "associates an interpretative annotation directly with a span"

## Content Model

```xml
<content>
    <alternate minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.stageLike"/>
      <classRef key="model.global"/>
      <classRef key="model.lLike"/>
      <classRef key="model.pLike"/>
      <classRef key="model.listLike"/>
      <classRef key="model.attributable"/>
      <elementRef key="speaker"/>
      <elementRef key="lg"/>
      <elementRef key="q"/>
    </alternate>
  </content>
```
