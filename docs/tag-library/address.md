# `<address>` Adresse

enthält eine Postadresse, z. B. eines Verlegers, einer Organisation oder einer Einzelperson.

Dieses Element sollte ausschließlich für
    postalische Addressen verwendet werden. Innerhalb des Elements
    kann das generische addrLine-Element als Alternative zu
    den spezielleren Elementen aus der model.addrPart-Klasse, wie street
    (Straße), postCode (Postleitzahl), etc. verwendet
    werden.

Siehe [Textstruktur > Unterschriften](https://dokumentation.karl-barth.ch/textstruktur/unterschriften/)

[TEI Guidelines: address](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-address.html)

**Modul:** core — Kernmodule

## Attribute

**@type** (optional, erweiterbar)
:   `billing`
:   `delivery`
:   `mailing`
:   `military`
:   `physical`

**@role** (optional)
:   Datentyp: teidata.enumerated
:   `sender`
:   `return`
:   `recipient `
:   `work`
:   `home`
:   `start`
:   `finish`
:   `pickup`
:   `dropOff`

**@rend** (optional)

**@rendition** (optional)


## Content Model

```xml
<content>
    <sequence>
      <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
      <sequence minOccurs="1" maxOccurs="unbounded">
        <classRef key="model.addrPart"/>
        <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
      </sequence>
    </sequence>
  </content>
```
