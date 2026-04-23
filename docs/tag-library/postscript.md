# `<postscript>`

enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief.

[TEI Guidelines: postscript](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-postscript.html)

**Modul:** textstructure — Textstruktur

## Enthalten in

**textstructure:** [body](body.md) "Enthält den gesamten Textkörper eines KBGA-Dokuments." [div](div.md) "Gliederungseinheit eines Textes. Der @type unterscheidet Tex" [postscript](postscript.md) "enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief."

**core:** [lg](lg.md) "Strophe oder Versgruppe." [list](list.md) "Liste. Der @type unterscheidet geordnete und ungeordnete Lis"

**figures:** [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik (" [table](table.md) "Tabelle."

## Kann enthalten

**textstructure:** [closer](closer.md) "Schlussformel eines Briefes (Gruss, Unterschrift, Datum)." [opener](opener.md) "fasst Datumszeile, Verfasserangabe, Anredeformel und ähnlich" [postscript](postscript.md) "enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief." [signed](signed.md) "enthält die abschließende Grußformel o.Ä. die ein Vorwort, e"

**core:** [address](address.md) "enthält eine Postadresse, z. B. eines Verlegers, einer Organ" [bibl](bibl.md) "Bibliographische Angabe. Unterscheidet zwischen gedruckter G" [cit](cit.md) "Zitat mit optionaler bibliographischer Angabe." [head](head.md) "Überschrift einer Gliederungseinheit (div)." [l](l.md) "Verszeile." [lb](lb.md) "markiert den Anfang einer neuen typographischen 
    Zeile i" [lg](lg.md) "Strophe oder Versgruppe." [list](list.md) "Liste. Der @type unterscheidet geordnete und ungeordnete Lis" [listBibl](listBibl.md) "enthält eine Liste von bibliografischen Angaben jeglicher Ar" [milestone](milestone.md) "markiert einen Grenzpunkt, der Abschnitte eines Textes trenn" [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo" [pb](pb.md) "Seitenumbruch. Das @ed unterscheidet die Ausgabe (pga, A), @" [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [sp](sp.md) "enthält eine einzelne Figurenrede in einem Dramentext oder e" [stage](stage.md) "enthält jegliche Regieanweisung in einem Dramentext oder -fr"

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati" [anchor](anchor.md) "Ankerpunkt für Querverweise (@type='cross') und für Fussnote"

**namesdates:** [listEvent](listEvent.md) "contains a list of descriptions, each of which provides info"

**figures:** [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik (" [table](table.md) "Tabelle."

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
"

**analysis:** [span](span.md) "associates an interpretative annotation directly with a span"

## Content Model

```xml
<content>
    <sequence>
      <alternate minOccurs="0" maxOccurs="unbounded">
	<classRef key="model.global"/>
	<classRef key="model.divTopPart"/>
      </alternate>
      <classRef key="model.common"/>
      <alternate minOccurs="0" maxOccurs="unbounded">
	<classRef key="model.global"/>
	<classRef key="model.common"/>
      </alternate>
      <sequence minOccurs="0" maxOccurs="unbounded">
	<classRef key="model.divBottomPart"/>
	<classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
      </sequence>
    </sequence>
  </content>
```
