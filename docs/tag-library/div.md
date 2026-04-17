# `<div/>` (Textabschnitt)

**Modul:** Textstruktur

## Beschreibung

Gliederungseinheit eines Textes. Der @type unterscheidet Textsorten (letter, sermon, speech etc.) und Strukturteile (opener, closer, abstract, songs).

## Erläuterung

Ausführliche Dokumentation:

- [Textstruktur > Gliederung](https://dokumentation.karl-barth.ch/textstruktur/gliederung/)

## Inhaltsmodell

- `<schemaSpec>`
- *model.divTop*
- *model.global*
- *model.divLike*
- *model.divGenLike*
- *model.global*
- *model.common*
- *model.global*
- *model.divLike*
- *model.divGenLike*
- *model.global*
- *model.divBottom*
- *model.global*

## Attribute

### `@type` (optional, erweiterbare Werteliste)

**Mögliche Werte:**

- `paper`
- `abstract`
- `excursus`
- `letter`
- `speech`
- `session`
- `chapter`
- `alternative-text` — Eine andere Version eines Textes.

### `@corresp` (optional)

Enthält eine xml:id eines korrespondierenden divs

## Constraints

**abstractModel-structure-div-in-l**
:   Abstract model violation: Metrical lines may not contain higher-level structural elements such as div, unless div is a descendant of floatingText.

**abstractModel-structure-div-in-ab-or-p**
:   Abstract model violation: p and ab may not contain higher-level structural elements such as div, unless div is a descendant of floatingText.

## Beispiele

**Beispiel 1:**

```xml
<div type="letter">
  <head>Brief Nr. 3</head>
  <opener>Lieber Herr Barth!</opener>
  <p>...</p>
  <closer>
    <salute>Mit herzlichem Gruß</salute>
    <signed><persName ref="kbga-actors-512">Rudolf Bultmann</persName></signed>
  </closer>
</div>
```

**Beispiel 2:**

```xml
<div type="abstract">
  <p>Zusammenfassung des Textes...</p>
</div>
```
