# `<head/>` (Überschrift)

**Modul:** Kernmodule

## Beschreibung

Überschrift einer Gliederungseinheit (div).

## Erläuterung

Ausführliche Dokumentation:

- [Textstruktur > Ueberschriften](https://dokumentation.karl-barth.ch/textstruktur/ueberschriften/)

## Inhaltsmodell

- Beliebiger Textinhalt
- [`<lg>`](lg.md)
- *model.gLike*
- *model.phrase*
- *model.inter*
- *model.lLike*
- *model.global*

## Beispiele

**Beispiel 1:**

```xml
<div1 n="I" type="book">
        <head>In the name of Christ here begins the first book of the ecclesiastical history of
          Georgius Florentinus, known as Gregory, Bishop of Tours.</head>
        <div2 type="section">
          <head>In the name of Christ here begins Book I of the history.</head>
          <p>Proposing as I do ...</p>
          <p>From the Passion of our Lord until the death of Saint Martin four hundred and twelve
            years passed.</p>
          <trailer>Here ends the first Book, which covers five thousand, five hundred and ninety-six
            years from the beginning of the world down to the death of Saint Martin.</trailer>
        </div2>
      </div1>
```

**Beispiel 2:**

```xml
With a few exceptions, connectives are equally
      useful in all kinds of discourse: description, narration, exposition, argument.
<list rend="bulleted">
  <head>Connectives</head>
  <item>above</item>
  <item>accordingly</item>
  <item>across from</item>
  <item>adjacent to</item>
  <item>again</item>
  <item>
    <!-- ... -->
  </item>
</list>
```
