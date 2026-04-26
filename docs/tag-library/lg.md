# `<lg>` Gruppe von Vers(zeil)en

Strophe oder Versgruppe.

Siehe [Textstruktur > Gedichte](https://dokumentation.karl-barth.ch/textstruktur/gedichte/)

[TEI Guidelines: lg](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-lg.html)

**Modul:** core — Kernmodule

## Attribute

**@xml:space** (optional)


## Enthalten in

**textstructure:** [argument](argument.md) "Zusammenfassung oder Regest eines Textes, typisch am Anfang " [body](body.md) "Enthält den gesamten Textkörper eines KBGA-Dokuments." [div](div.md) "Gliederungseinheit eines Textes. Der @type unterscheidet Tex" [epigraph](epigraph.md) "enthält ein anonymes oder jemandem zugeschriebenes Zitat, da" [postscript](postscript.md) "enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief." [salute](salute.md) "enthält eine Anrede oder Grußformel, die einem Vorwort, eine" [signed](signed.md) "enthält die abschließende Grußformel o.Ä. die ein Vorwort, e"

**core:** [corr](corr.md) "Korrektur eines Fehlers in der Druckausgabe. Der @type unter" [head](head.md) "Überschrift einer Gliederungseinheit (div)." [hi](hi.md) "Hervorhebung. Das @rend gibt die Art an (italic, bold, sup, " [item](item.md) "enthält einen Listenpunkt." [lg](lg.md) "Strophe oder Versgruppe." [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo" [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L" [sic](sic.md) "Markiert die fehlerhafte Stelle in der Druckausgabe (innerha" [sp](sp.md) "enthält eine einzelne Figurenrede in einem Dramentext oder e" [stage](stage.md) "enthält jegliche Regieanweisung in einem Dramentext oder -fr" [title](title.md) "Titel mit verschiedenen Funktionen, unterschieden durch @typ"

**header:** [change](change.md) "Änderungsvermerk in der revisionDesc. Enthält Zeitstempel de" [licence](licence.md) "beinhaltet für den Text gültige Lizenzinformationen oder and"

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati" [seg](seg.md) "Segment. Verwendet für nicht-Entitäten, Verse, Biogramme, He"

**figures:** [cell](cell.md) "Tabellenzelle." [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik ("

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
"

## Kann enthalten

**textstructure:** [argument](argument.md) "Zusammenfassung oder Regest eines Textes, typisch am Anfang " [closer](closer.md) "Schlussformel eines Briefes (Gruss, Unterschrift, Datum)." [dateline](dateline.md) "enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw." [docDate](docDate.md) "enthält die Datierung des Dokuments, wie auf der Titelseite " [epigraph](epigraph.md) "enthält ein anonymes oder jemandem zugeschriebenes Zitat, da" [opener](opener.md) "fasst Datumszeile, Verfasserangabe, Anredeformel und ähnlich" [postscript](postscript.md) "enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief." [salute](salute.md) "enthält eine Anrede oder Grußformel, die einem Vorwort, eine" [signed](signed.md) "enthält die abschließende Grußformel o.Ä. die ein Vorwort, e"

**core:** [address](address.md) "enthält eine Postadresse, z. B. eines Verlegers, einer Organ" [corr](corr.md) "Korrektur eines Fehlers in der Druckausgabe. Der @type unter" [head](head.md) "Überschrift einer Gliederungseinheit (div)." [l](l.md) "Verszeile." [lb](lb.md) "markiert den Anfang einer neuen typographischen 
    Zeile i" [lg](lg.md) "Strophe oder Versgruppe." [milestone](milestone.md) "markiert einen Grenzpunkt, der Abschnitte eines Textes trenn" [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [pb](pb.md) "Seitenumbruch. Das @ed unterscheidet die Ausgabe (pga, A), @" [sic](sic.md) "Markiert die fehlerhafte Stelle in der Druckausgabe (innerha" [stage](stage.md) "enthält jegliche Regieanweisung in einem Dramentext oder -fr"

**linking:** [anchor](anchor.md) "Ankerpunkt für Querverweise (@type='cross') und für Fussnote"

**figures:** [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik ("

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
"

**analysis:** [span](span.md) "associates an interpretative annotation directly with a span"

## Constraints

**atleast1oflggapl**
:   An lg element must contain at least one child l, lg, or gap element.

**abstractModel-structure-lg-in-l**
:   Abstract model violation: Lines may not contain line groups.

## Content Model

```xml
<content>
  <sequence minOccurs="1" maxOccurs="1">
    <alternate minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.divTop"/>
      <classRef key="model.global"/>
    </alternate>
    <alternate minOccurs="1" maxOccurs="1">
      <classRef key="model.lLike"/>
      <classRef key="model.stageLike"/>
      <classRef key="model.labelLike"/>
      <classRef key="model.pPart.transcriptional"/>
      <elementRef key="lg"/>
    </alternate>
    <alternate minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.lLike"/>
      <classRef key="model.stageLike"/>
      <classRef key="model.labelLike"/>
      <classRef key="model.pPart.transcriptional"/>
      <classRef key="model.global"/>
      <elementRef key="lg"/>
    </alternate>
    <sequence minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.divBottom"/>
      <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
    </sequence>
  </sequence>
</content>
```
