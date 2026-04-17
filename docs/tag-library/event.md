# `<event>` Ereignis

enthält Daten mit Bezug zu etwas Bemerkenswertem, das in der Zeit geschieht.

**Modul:** namesdates — Namen und Daten

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


**att.datable** provides attributes for normalization of elements
    that contain dates, times, or datable events.

**@period** (optional)
:   Datentyp: teidata.pointer


**att.locatable** provides attributes for referencing locations by pointing to entries in a canonical list of places.

**@where** (optional)
:   Datentyp: teidata.pointer


**att.naming** provides attributes common to elements which refer to named persons, places, organizations etc.

**@role** (optional)
:   Datentyp: teidata.enumerated


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


## Kann enthalten

**header:** [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer."

## Content Model

```xml
<content>
    <sequence>
      <elementRef key="idno" minOccurs="0" maxOccurs="unbounded"/>
      <classRef key="model.headLike" minOccurs="0" maxOccurs="unbounded"/>
      <alternate>
        <classRef key="model.pLike" minOccurs="1" maxOccurs="unbounded"/>
        <classRef key="model.labelLike" minOccurs="1" maxOccurs="unbounded"/>
        <elementRef key="eventName" minOccurs="1" maxOccurs="unbounded"/>
      </alternate>
      <alternate minOccurs="0" maxOccurs="unbounded">
        <classRef key="model.noteLike"/>
        <classRef key="model.biblLike"/>
        <classRef key="model.ptrLike"/>
        <elementRef key="linkGrp"/>
        <elementRef key="link"/>
        <elementRef key="idno"/>
      </alternate>
      <classRef key="model.eventLike" minOccurs="0" maxOccurs="unbounded"/>
      <alternate minOccurs="0" maxOccurs="unbounded">
        <classRef key="model.personLike" minOccurs="1" maxOccurs="1"/>
        <elementRef key="listPerson" minOccurs="1" maxOccurs="1"/>
      </alternate>
      <alternate minOccurs="0" maxOccurs="unbounded">
        <classRef key="model.placeLike" minOccurs="1" maxOccurs="1"/>
        <elementRef key="listPlace" minOccurs="1" maxOccurs="1"/>
      </alternate>
      <classRef key="model.objectLike" minOccurs="0" maxOccurs="unbounded"/>
      <alternate minOccurs="0" maxOccurs="unbounded">
        <elementRef key="relation" minOccurs="1" maxOccurs="1"/>
        <elementRef key="listRelation" minOccurs="1" maxOccurs="1"/>
      </alternate>
    </sequence>
  </content>
```
