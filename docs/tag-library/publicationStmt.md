# `<publicationStmt>` Angaben zur Veröffentlichung

umfasst Angaben zu Veröffentlichung oder Vertrieb eines elektronischen oder sonstigen Textes.

Wenn die Angaben zur Veröffentlichung mehrere Mitglieder der Klassen model.publicationStmtPart.agency oder model.publicationStmtPart.detail  
          enthalten und nicht einen oder mehrere Absätze (p) bzw. unbestimmte Einheiten (ab), dann hat 
          die Reihenfolge der Elemente eine Bedeutung, auf die zu achten ist. So müssen Elemente, die Angaben über den Veröffentlichungsort, 
          die Adresse, den Identifikator, die Verfügbarkeit und das Veröffentlichungsdatum enthalten, auf den Namen des Verlags, des 
          Distributors oder der Freigabeinstanz folgen, und zwar möglichst in dieser Reihenfolge.

**Modul:** header — Header

## Attribute

**att.global** stellt gemeinsame Attribute für alle Elemente im TEI-Kodierungsschema bereit.

**@xml:id** (optional)
:   liefert einen Identifikator für das Element, welches dieses Attribut trägt.
:   Datentyp: ID

**@n** (optional)
:   gibt eine Nummer (oder eine andere Bezeichnung) für ein Element an, die innerhalb des Dokuments nicht zwangsläufig eindeutig ist.
:   Datentyp: teidata.text

**@xml:lang** (optional)
:   gibt die Sprache des Elementinhalts durch ein Tag an, das nach BCP 47 festgelegt wird.
:   Datentyp: teidata.language

**@xml:base** (optional)
:   liefert eine Basis-URI-Referenz, mit der Anwendungen relative URI-Referenzen in absolute auflösen können.
:   Datentyp: teidata.pointer

**@xml:space** (optional, geschlossene Werteliste)
:   signalisiert die gewünschte Handhabung von Leerzeichen durch Anwendungen.
:   Datentyp: teidata.enumerated
:   `default`
:   `preserve`


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
