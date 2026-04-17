# `<msItem>`

describes an individual work or item within the intellectual
  content of a manuscript, manuscript part, or other object.

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

**msdescription:** [msContents](msContents.md) "describes the intellectual content of a manuscript, manuscri"

## Content Model

```xml
<content>
    <sequence>
      
        <alternate minOccurs="0" maxOccurs="unbounded">
          <elementRef key="locus"/>
          <elementRef key="locusGrp"/>
        </alternate>
      
      <alternate>
        
          <classRef key="model.pLike" minOccurs="1" maxOccurs="unbounded"/>
        
        
          <alternate minOccurs="1" maxOccurs="unbounded">
            <classRef key="model.titlepagePart"/>
            <classRef key="model.msItemPart"/>
            <classRef key="model.global"/>
          </alternate>
        
      </alternate>
    </sequence>
  </content>
```
