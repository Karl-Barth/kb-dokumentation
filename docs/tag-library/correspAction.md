# `<correspAction>`

contains a structured
  description of the place, the name of a person/organization and the
  date related to the sending/receiving of a message or any other
  action related to the correspondence.

[TEI Guidelines: correspAction](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-correspAction.html)

**Modul:** header — Header

## Attribute

**@type** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `sent`
:   `received`
:   `transmitted`
:   `redirected`
:   `forwarded`


## Enthalten in

**header:** [correspDesc](correspDesc.md) "contains a description
    of the actions related to one act"

## Kann enthalten

**core:** [address](address.md) "enthält eine Postadresse, z. B. eines Verlegers, einer Organ" [date](date.md) "Datumsangabe mit maschinenlesbarem Datum in @when, @from/@to" [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo" [rs](rs.md) "Referenzierende Zeichenkette für Akteure, die nicht als pers"

**header:** [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer."

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati"

**namesdates:** [orgName](orgName.md) "Name einer Organisation mit Verweis auf die Meta-DB via @ref" [persName](persName.md) "Personenname mit Verweis auf die Meta-DB via @ref (kbga-acto" [placeName](placeName.md) "Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-I"

## Content Model

```xml
<content>
    <alternate>
      <classRef key="model.correspActionPart" minOccurs="1" maxOccurs="unbounded"/>
      <classRef key="model.pLike" minOccurs="1" maxOccurs="unbounded"/>
    </alternate>
  </content>
```
