# `<msContents>`

describes the intellectual content of a manuscript, manuscript
    part, or other object either as a series of paragraphs or as a series of structured manuscript items.

**Modul:** msdescription — Handschriftenbeschreibung

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

**msdescription:** [msDesc](msDesc.md) "contains a description of a single identifiable
    manuscri"

## Kann enthalten

**msdescription:** [msItem](msItem.md) "describes an individual work or item within the intellectual"

## Content Model

```xml
<content>
    <alternate>
      
        <classRef key="model.pLike" minOccurs="1" maxOccurs="unbounded"/>
      
      <sequence>
        
          <elementRef key="summary" minOccurs="0"/>
        
        
          <elementRef key="textLang" minOccurs="0"/>
        
        
          <elementRef key="titlePage" minOccurs="0"/>
        
        
          <alternate minOccurs="0" maxOccurs="unbounded">
            <elementRef key="msItem"/>
            <elementRef key="msItemStruct"/>
          </alternate>
        
      </sequence>
    </alternate>
  </content>
```
