# `<address>` Adresse

enthält eine Postadresse, z. B. eines Verlegers, einer Organisation oder einer Einzelperson.

Dieses Element sollte ausschließlich für
    postalische Addressen verwendet werden. Innerhalb des Elements
    kann das generische addrLine-Element als Alternative zu
    den spezielleren Elementen aus der model.addrPart-Klasse, wie street
    (Straße), postCode (Postleitzahl), etc. verwendet
    werden.

Siehe [Textstruktur > Unterschriften](https://dokumentation.karl-barth.ch/textstruktur/unterschriften/)

**Modul:** core — Kernmodule

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


**att.canonical** provides attributes that can be used to associate a representation such as a name or title
    with canonical information about the object being named or referenced.

**@key** (optional)
:   Datentyp: teidata.text

**@ref** (optional)
:   Datentyp: teidata.pointer


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


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
