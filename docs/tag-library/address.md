# `<address/>` (Adresse)

**Modul:** Kernmodule

## Beschreibung

enthält eine Postadresse, z. B. eines Verlegers, einer Organisation oder einer Einzelperson.

!!! note "Ausführliche Dokumentation"
    [Textstruktur > Unterschriften](https://dokumentation.karl-barth.ch/textstruktur/unterschriften/)


## Inhaltsmodell

- *model.global*
- *model.addrPart*
- *model.global*

## Attribute

### `@type` (erweiterbare Werteliste)

**Mögliche Werte:**

- `billing`
- `delivery`
- `mailing`
- `military`
- `physical`

### `@role`

**Datentyp:** `teidata.enumerated`

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
