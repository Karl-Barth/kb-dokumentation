# `<fileDesc>` Dateibeschreibung

enthält die vollständige bibliografische Beschreibung einer elektronischen Datei.

Die wesentliche Informationsquelle für die Erstellung eines Katalogeintrags oder eines bibliografischen 
          Zitats einer elektronischen Datei. Das Element liefert einen Titel und Angaben zu Verantwortlichkeiten 
          zusammen mit Details zu Publikation und Distribution der Datei, sowie eine mögliche Zugehörigkeit zu einer Reihe. 
          Außerdem kann es detaillierte bibliografische Anmerkungen für Sachverhalte, die an keiner anderen Stelle im TEI-Header 
          behandelt werden können, enthalten. Es beinhaltet außerdem eine vollständige bibliografische Beschreibung der 
          Quelle selbst bzw. der Quellen von welchen sich der elektronische Text ableitet.

**Modul:** header — Header

## Enthalten in

**header:** [teiHeader](teiHeader.md) "wird aus der Meta- und Registerdatenbank erzeugt und soll im"

## Kann enthalten

**header:** [editionStmt](editionStmt.md) "Angaben zur digitalen Edition (Titel, Förderer)." [publicationStmt](publicationStmt.md) "umfasst Angaben zu Veröffentlichung oder Vertrieb eines elek" [sourceDesc](sourceDesc.md) "beschreibt die Quelle, von der sich der elektronische Text a" [titleStmt](titleStmt.md) "sollte mehrere Titel für verschiedene Zwecke enhalten."

## Content Model

```xml
<content>
    <sequence>
      <sequence>
        <elementRef key="titleStmt"/>
        
          <elementRef key="editionStmt" minOccurs="0"/>
        
        
          <elementRef key="extent" minOccurs="0"/>
        
        <elementRef key="publicationStmt"/>
        
          <elementRef key="seriesStmt" minOccurs="0" maxOccurs="unbounded"/>
        
        
          <elementRef key="notesStmt" minOccurs="0"/>
        
      </sequence>
      
        <elementRef key="sourceDesc" minOccurs="1" maxOccurs="unbounded"/>
      
    </sequence>
  </content>
```
