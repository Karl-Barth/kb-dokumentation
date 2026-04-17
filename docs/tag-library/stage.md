# `<stage/>` (Regieanweisung)

**Modul:** Kernmodule

## Beschreibung

enthält jegliche Regieanweisung in einem Dramentext oder -fragment.

## Erläuterung

Das who-Attribut kann verwendet werden, um die Person oder Personen näher zu
      bezeichnen, die die Regieanweisung ausführen.

## Inhaltsmodell

- *macro.specialPara*

## Attribute

### `@type` (optional, erweiterbare Werteliste)

beschreibt die Art der Regieanweisung.

**Datentyp:** teidata.enumerated

**Mögliche Werte:**

- `setting` — beschreibt die Szenerie.
- `entrance` — beschreibt einen Auftritt.
- `exit` — beschreibt einen Abgang.
- `business` — beschreibt eine Bühnenhandlung.
- `novelistic` — beschreibt eine narrative Regieanweisung.
- `delivery` — beschreibt die Art und Weise der Darbietung einer Figurenrede.
- `modifier` — gibt nähere Details zu einer Figur an.
- `location` — beschreibt einen Handlungsort.
- `mixed` — mehrere der oben angeführten Funktionen.
