# `<availability>` Verfügbarkeit

Lizenzinformationen zur Publikation. Wird aus der Datenbank generiert.

Es sollte ein einheitliches Format verwendet werden.

[TEI Guidelines: availability](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-availability.html)

**Modul:** header — Header

## Enthalten in

**core:** [bibl](bibl.md) "Bibliographische Angabe. Unterscheidet zwischen gedruckter G"

**header:** [publicationStmt](publicationStmt.md) "umfasst Angaben zu Veröffentlichung oder Vertrieb eines elek"

## Kann enthalten

**core:** [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo"

**header:** [licence](licence.md) "beinhaltet für den Text gültige Lizenzinformationen oder and"

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati"

## Content Model

```xml
<content>
  <alternate minOccurs="1" maxOccurs="unbounded">
    <classRef key="model.availabilityPart"/>
    <classRef key="model.pLike"/>
  </alternate>
</content>
```
