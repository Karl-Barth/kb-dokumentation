# `<msIdentifier>`

contains the information required to identify the manuscript or similar object being described.

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

**header:** [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer."

**msdescription:** [altIdentifier](altIdentifier.md) "Alternativer Identifikator für eine Quelle (URI, KBA-ID, KBG" [repository](repository.md) "contains the name of a repository within which manuscripts o"

## Constraints

**msId_minimal**
:   An msIdentifier must contain either a repository or location.

## Content Model

```xml
<content>
    <sequence>
      <sequence>
        <classRef key="model.placeNamePart" expand="sequenceOptional"/>        
        <elementRef key="institution" minOccurs="0"/>
        <elementRef key="repository" minOccurs="0"/>
        <elementRef key="collection" minOccurs="0" maxOccurs="unbounded"/>
        <elementRef key="idno" minOccurs="0" maxOccurs="unbounded"/>
      </sequence>
      <alternate minOccurs="0" maxOccurs="unbounded">
        <elementRef key="msName"/>
        <elementRef key="objectName"/>
        <elementRef key="altIdentifier"/>
      </alternate>
    </sequence>
  </content>
```
