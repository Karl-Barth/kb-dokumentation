# `<address/>` (Adresse)

**Modul:** Kernmodule

## Beschreibung

enthält eine Postadresse, z. B. eines Verlegers, einer Organisation oder einer Einzelperson.

## Erläuterung

Dieses Element sollte ausschließlich für
    postalische Addressen verwendet werden. Innerhalb des Elements
    kann das generische addrLine-Element als Alternative zu
    den spezielleren Elementen aus der model.addrPart-Klasse, wie street
    (Straße), postCode (Postleitzahl), etc. verwendet
    werden.

Ausführliche Dokumentation:

- [Textstruktur > Unterschriften](https://dokumentation.karl-barth.ch/textstruktur/unterschriften/)

## Inhaltsmodell

- *model.global*
- *model.addrPart*
- *model.global*

## Attribute

### `@type` (optional, erweiterbare Werteliste)

**Mögliche Werte:**

- `billing`
- `delivery`
- `mailing`
- `military`
- `physical`

### `@role` (optional)

**Datentyp:** teidata.enumerated

**Mögliche Werte:**

- `sender`
- `return`
- `recipient `
- `work`
- `home`
- `start`
- `finish`
- `pickup`
- `dropOff`
