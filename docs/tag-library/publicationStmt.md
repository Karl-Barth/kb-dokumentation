# `<publicationStmt>` Angaben zur Veröffentlichung

umfasst Angaben zu Veröffentlichung oder Vertrieb eines elektronischen oder sonstigen Textes.

Wenn die Angaben zur Veröffentlichung mehrere Mitglieder der Klassen model.publicationStmtPart.agency oder model.publicationStmtPart.detail  
          enthalten und nicht einen oder mehrere Absätze (p) bzw. unbestimmte Einheiten (ab), dann hat 
          die Reihenfolge der Elemente eine Bedeutung, auf die zu achten ist. So müssen Elemente, die Angaben über den Veröffentlichungsort, 
          die Adresse, den Identifikator, die Verfügbarkeit und das Veröffentlichungsdatum enthalten, auf den Namen des Verlags, des 
          Distributors oder der Freigabeinstanz folgen, und zwar möglichst in dieser Reihenfolge.

[TEI Guidelines: publicationStmt](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-publicationStmt.html)

**Modul:** header — Header

## Enthalten in

**header:** [fileDesc](fileDesc.md) "enthält die vollständige bibliografische Beschreibung einer "

## Content Model

```xml
<content>
    <alternate>
      
	<sequence minOccurs="1" maxOccurs="unbounded">
	  
	    <classRef key="model.publicationStmtPart.agency"/>
	  
	  
	    <classRef key="model.publicationStmtPart.detail" minOccurs="0" maxOccurs="unbounded"/>
	  
	</sequence>
      
      
	<classRef key="model.pLike" minOccurs="1" maxOccurs="unbounded"/>
      
    </alternate>
  </content>
```
