# `<listEvent>`

contains a list of descriptions, each of which provides information about an identifiable event.

[TEI Guidelines: listEvent](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listEvent.html)

**Modul:** namesdates — Namen und Daten

## Enthalten in

**textstructure:** [argument](argument.md) "Zusammenfassung oder Regest eines Textes, typisch am Anfang " [body](body.md) "Enthält den gesamten Textkörper eines KBGA-Dokuments." [div](div.md) "Gliederungseinheit eines Textes. Der @type unterscheidet Tex" [epigraph](epigraph.md) "enthält ein anonymes oder jemandem zugeschriebenes Zitat, da" [postscript](postscript.md) "enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief." [salute](salute.md) "enthält eine Anrede oder Grußformel, die einem Vorwort, eine" [signed](signed.md) "enthält die abschließende Grußformel o.Ä. die ein Vorwort, e"

**core:** [corr](corr.md) "Korrektur eines Fehlers in der Druckausgabe. Der @type unter" [head](head.md) "Überschrift einer Gliederungseinheit (div)." [hi](hi.md) "Hervorhebung. Das @rend gibt die Art an (italic, bold, sup, " [item](item.md) "enthält einen Listenpunkt." [l](l.md) "Verszeile." [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo" [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [quote](quote.md) "Zitat innerhalb des Textes." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L" [sic](sic.md) "Markiert die fehlerhafte Stelle in der Druckausgabe (innerha" [sp](sp.md) "enthält eine einzelne Figurenrede in einem Dramentext oder e" [stage](stage.md) "enthält jegliche Regieanweisung in einem Dramentext oder -fr" [title](title.md) "Titel mit verschiedenen Funktionen, unterschieden durch @typ"

**header:** [change](change.md) "Änderungsvermerk in der revisionDesc. Enthält Zeitstempel de" [licence](licence.md) "beinhaltet für den Text gültige Lizenzinformationen oder and" [sourceDesc](sourceDesc.md) "beschreibt die Quelle, von der sich der elektronische Text a"

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati" [seg](seg.md) "Segment. Verwendet für nicht-Entitäten, Verse, Biogramme, He"

**namesdates:** [event](event.md) "enthält Daten mit Bezug zu etwas Bemerkenswertem, das in der" [listEvent](listEvent.md) "contains a list of descriptions, each of which provides info"

**figures:** [cell](cell.md) "Tabellenzelle." [figDesc](figDesc.md) "enthält einen kurzen Beschreibungstext des Inhalts oder des " [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik ("

**transcr:** [metamark](metamark.md) "contains or describes any kind of graphic or written signal
"

## Kann enthalten

**core:** [head](head.md) "Überschrift einer Gliederungseinheit (div)."

**namesdates:** [event](event.md) "enthält Daten mit Bezug zu etwas Bemerkenswertem, das in der" [listEvent](listEvent.md) "contains a list of descriptions, each of which provides info"

## Content Model

```xml
<content>
    <sequence>
      <classRef key="model.headLike" minOccurs="0" maxOccurs="unbounded"/>
      <elementRef key="desc" minOccurs="0" maxOccurs="unbounded"/>
      <alternate minOccurs="0" maxOccurs="unbounded">
        <elementRef key="relation" minOccurs="1" maxOccurs="1"/>
        <elementRef key="listRelation" minOccurs="1" maxOccurs="1"/>
      </alternate>
      <sequence minOccurs="1" maxOccurs="unbounded">
        <classRef key="model.eventLike" minOccurs="1" maxOccurs="unbounded"/>
        <alternate minOccurs="0" maxOccurs="unbounded">
          <elementRef key="relation" minOccurs="1" maxOccurs="1"/>
          <elementRef key="listRelation" minOccurs="1" maxOccurs="1"/>
        </alternate>
      </sequence>
    </sequence>
  </content>
```
