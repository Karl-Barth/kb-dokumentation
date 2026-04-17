# `<corr/>` (Korrektur)

**Modul:** Kernmodule

## Beschreibung

Korrektur eines Fehlers in der Druckausgabe. Der @type unterscheidet inhaltliche Korrekturen (corr), Druckfehler (misprint) und veraltete Angaben (update).

!!! note "Ausführliche Dokumentation"
    [Textelemente > Korrektionen Der Druckausgabe](https://dokumentation.karl-barth.ch/textelemente/korrektionen-der-druckausgabe/)


## Inhaltsmodell

- *macro.paraContent*

## Attribute

### `@type` (geschlossene Werteliste)

**Mögliche Werte:**

- `corr` — korrigiert einen inhaltlichen Fehler
- `misprint` — korrigiert einen Druckfehler
- `update` — wenn Angaben veraltet sind, z.B. URLs
