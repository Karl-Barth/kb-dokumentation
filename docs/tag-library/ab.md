# `<ab>`

Anonymer Block, verwendet für zentrierte oder anders formatierte Textabschnitte ohne Absatz-Semantik.

Siehe [Textstruktur > Absatz](https://dokumentation.karl-barth.ch/textstruktur/absatz/)

**Modul:** linking — Linking

## Constraints

**abstractModel-structure-ab-in-l**
:   Abstract model violation: Metrical lines may not contain higher-level divisions such as p or ab, unless ab is a child of figure or note, or is a descendant of floatingText.

## Beispiele

```xml
<ab rend="center">* * *</ab>
```

## Content Model

```xml
<content>
  <macroRef key="macro.abContent"/>
</content>
```
