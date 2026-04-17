# `<correspAction>`

contains a structured
  description of the place, the name of a person/organization and the
  date related to the sending/receiving of a message or any other
  action related to the correspondence.

**Modul:** header — Header

## Attribute

**@type** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `sent`
:   `received`
:   `transmitted`
:   `redirected`
:   `forwarded`


## Content Model

```xml
<content>
    <alternate>
      <classRef key="model.correspActionPart" minOccurs="1" maxOccurs="unbounded"/>
      <classRef key="model.pLike" minOccurs="1" maxOccurs="unbounded"/>
    </alternate>
  </content>
```
