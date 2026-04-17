# `<event>` Ereignis

enthält Daten mit Bezug zu etwas Bemerkenswertem, das in der Zeit geschieht.

**Modul:** namesdates — Namen und Daten

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
