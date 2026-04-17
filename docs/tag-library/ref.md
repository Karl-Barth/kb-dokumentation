# `<ref/>` (Referenz)

**Modul:** Kernmodule

## Beschreibung

Verweis auf eine andere Ressource. Dient für Bibelstellen, Literaturverweise, Querverweise und URLs.

## Erläuterung

Ausführliche Dokumentation:

- [Textelemente > Querverweise](https://dokumentation.karl-barth.ch/textelemente/querverweise/)

## Inhaltsmodell

- *macro.paraContent*

## Constraints

**ref1**
:   ref1: ref darf nicht in ref vorkommen.

**ref2**
:   ref2: @target in ref[@subtype='bibl'] darf kein Komma oder Bindestrich enthalten.

**refAtts**
:   Only one of the attributes @target and @cRef may be supplied on .

## Beispiele

**Beispiel 1:**

```xml
<ref type="pub" target="1005">Nr. 3</ref>
```

**Beispiel 2:**

```xml
<ref target="https://kba.karl-barth.ch/objects/7950">KBA 9311.73</ref>
```

**Beispiel 3:**

```xml
<ref type="can" subtype="bible" target="Röm.1.17">Röm. 1,17</ref>
```
