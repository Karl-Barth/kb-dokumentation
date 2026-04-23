# `<event>` Ereignis

enthält Daten mit Bezug zu etwas Bemerkenswertem, das in der Zeit geschieht.

[TEI Guidelines: event](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-event.html)

**Modul:** namesdates — Namen und Daten

## Enthalten in

**namesdates:** [event](event.md) "enthält Daten mit Bezug zu etwas Bemerkenswertem, das in der" [listEvent](listEvent.md) "contains a list of descriptions, each of which provides info"

## Kann enthalten

**core:** [bibl](bibl.md) "Bibliographische Angabe. Unterscheidet zwischen gedruckter G" [head](head.md) "Überschrift einer Gliederungseinheit (div)." [listBibl](listBibl.md) "enthält eine Liste von bibliografischen Angaben jeglicher Ar" [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo" [ptr](ptr.md) "defines a pointer to another location." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L"

**header:** [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer."

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati"

**namesdates:** [event](event.md) "enthält Daten mit Bezug zu etwas Bemerkenswertem, das in der" [listEvent](listEvent.md) "contains a list of descriptions, each of which provides info"

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
