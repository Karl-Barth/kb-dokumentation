# `<corr/>` (Korrektur)

**Modul:** Kernmodule

## Beschreibung

Korrektur eines Fehlers in der Druckausgabe. Der @type unterscheidet inhaltliche Korrekturen (corr), Druckfehler (misprint) und veraltete Angaben (update).

## Erläuterung

Ausführliche Dokumentation:

- [Textelemente > Korrektionen Der Druckausgabe](https://dokumentation.karl-barth.ch/textelemente/korrektionen-der-druckausgabe/)

## Inhaltsmodell

- *macro.paraContent*

## Attribute

### `@type` (optional, geschlossene Werteliste)

**Mögliche Werte:**

- `corr` — korrigiert einen inhaltlichen Fehler
- `misprint` — korrigiert einen Druckfehler
- `update` — wenn Angaben veraltet sind, z.B. URLs

## Beispiele

**Beispiel 1:**

```xml
I don't know,
      Juan. It's so far in the past now — how
<corr>can we</corr> prove
      or disprove anyone's theories?
```

**Beispiel 2:**

```xml
I don't know, Juan. It's so far in the past now —
      how
<choice>
  <sic>we can</sic>
  <corr>can we</corr>
</choice> prove or
      disprove anyone's theories?
```
