# `<editionStmt>` Angaben zur Ausgabe

Angaben zur digitalen Edition (Titel, Förderer).

[TEI Guidelines: editionStmt](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-editionStmt.html)

**Modul:** header — Header

## Enthalten in

**header:** [fileDesc](fileDesc.md) "enthält die vollständige bibliografische Beschreibung einer "

## Kann enthalten

**core:** [author](author.md) "Verfasserangabe im teiHeader. Das @ref verweist auf die Pers" [editor](editor.md) "Herausgeberangabe in einer bibliographischen Referenz." [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo"

**header:** [edition](edition.md) "beschreibt die Details einer Ausgabe eines Textes." [sponsor](sponsor.md) "gibt den Namen einer Organisation oder Institution an, die a"

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati"

## Content Model

```xml
<content>
  <alternate minOccurs="1" maxOccurs="1">
    <classRef key="model.pLike" minOccurs="1" maxOccurs="unbounded"/>
    <sequence minOccurs="1" maxOccurs="1">
      <elementRef key="edition"/>
      <classRef key="model.respLike" minOccurs="0" maxOccurs="unbounded"/>
    </sequence>
  </alternate>
</content>
```
