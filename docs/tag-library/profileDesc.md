# `<profileDesc>` Beschreibung des Textprofils

enthält eine detaillierte Beschreibung der nicht-bibliografischen Merkmale des Textes, besonders der verwendeten Sprachen und Subsprachen, 
        der Entstehungsbedingungen eines Textes sowie der Beteiligten und deren Umfeld.

Obwohl durch das Inhaltsmodell erlaubt, erscheint es in den seltensten Fällen sinnvoll, mehrere Vorkommen der erlaubten Kindelemente der profileDesc zu notieren – außer diese beziehen sich auf unterschiedliche Texte.

[TEI Guidelines: profileDesc](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-profileDesc.html)

**Modul:** header — Header

## Enthalten in

**header:** [teiHeader](teiHeader.md) "wird aus der Meta- und Registerdatenbank erzeugt und soll im"

## Kann enthalten

**header:** [correspDesc](correspDesc.md) "contains a description
    of the actions related to one act" [creation](creation.md) "beinhaltet Informationen zur Entstehung eines Textes." [langUsage](langUsage.md) "beschreibt Sprachen, Subsprachen, Register, Dialekte usw., d" [textClass](textClass.md) "gruppiert Informationen über Art oder Thematik eines Textes "

## Content Model

```xml
<content>
    
      
        <classRef key="model.profileDescPart" minOccurs="0" maxOccurs="unbounded"/>
      
    
  </content>
```
