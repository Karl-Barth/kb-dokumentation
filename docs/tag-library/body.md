# `<body>` Textkörper

Enthält den gesamten Textkörper eines KBGA-Dokuments.

[TEI Guidelines: body](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-body.html)

**Modul:** textstructure — Textstruktur

## Enthalten in

**textstructure:** [text](text.md) "enthält einen einzelnen, eigenständigen oder kompilierten Te"

## Kann enthalten

**textstructure:** [argument](argument.md) "Zusammenfassung oder Regest eines Textes, typisch am Anfang " [closer](closer.md) "Schlussformel eines Briefes (Gruss, Unterschrift, Datum)." [dateline](dateline.md) "enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw." [div](div.md) "Gliederungseinheit eines Textes. Der @type unterscheidet Tex" [docDate](docDate.md) "enthält die Datierung des Dokuments, wie auf der Titelseite " [epigraph](epigraph.md) "enthält ein anonymes oder jemandem zugeschriebenes Zitat, da" [opener](opener.md) "fasst Datumszeile, Verfasserangabe, Anredeformel und ähnlich" [postscript](postscript.md) "enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief." [salute](salute.md) "enthält eine Anrede oder Grußformel, die einem Vorwort, eine" [signed](signed.md) "enthält die abschließende Grußformel o.Ä. die ein Vorwort, e"

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
  <sequence minOccurs="1" maxOccurs="1">
    <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
    <sequence minOccurs="0" maxOccurs="1">
      <classRef key="model.divTop"/>
      <alternate minOccurs="0" maxOccurs="unbounded">
        <classRef key="model.global"/>
        <classRef key="model.divTop"/>
      </alternate>
    </sequence>
    <sequence minOccurs="0" maxOccurs="1">
      <classRef key="model.divGenLike"/>
      <alternate minOccurs="0" maxOccurs="unbounded">
        <classRef key="model.global"/>
        <classRef key="model.divGenLike"/>
      </alternate>
    </sequence>
    <alternate minOccurs="1" maxOccurs="1">
      <sequence minOccurs="1" maxOccurs="unbounded">
        <classRef key="model.divLike"/>
        <alternate minOccurs="0" maxOccurs="unbounded">
          <classRef key="model.global"/>
          <classRef key="model.divGenLike"/>
        </alternate>
      </sequence>
      <sequence minOccurs="1" maxOccurs="unbounded">
        <classRef key="model.div1Like"/>
        <alternate minOccurs="0" maxOccurs="unbounded">
          <classRef key="model.global"/>
          <classRef key="model.divGenLike"/>
        </alternate>
      </sequence>
      <sequence minOccurs="1" maxOccurs="1">
        <sequence minOccurs="1" maxOccurs="unbounded">
          <alternate minOccurs="1" maxOccurs="1">
            <elementRef key="schemaSpec"/>
            <classRef key="model.common"/>
          </alternate>
          <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
        </sequence>
        <alternate minOccurs="0" maxOccurs="1">
          <sequence minOccurs="1" maxOccurs="unbounded">
            <classRef key="model.divLike"/>
            <alternate minOccurs="0" maxOccurs="unbounded">
              <classRef key="model.global"/>
              <classRef key="model.divGenLike"/>
            </alternate>
          </sequence>
          <sequence minOccurs="1" maxOccurs="unbounded">
            <classRef key="model.div1Like"/>
            <alternate minOccurs="0" maxOccurs="unbounded">
              <classRef key="model.global"/>
              <classRef key="model.divGenLike"/>
            </alternate>
          </sequence>
        </alternate>
      </sequence>
    </alternate>
    <sequence minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.divBottom"/>
      <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
    </sequence>
  </sequence>
</content>
```
