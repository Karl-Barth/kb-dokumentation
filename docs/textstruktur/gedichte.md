# Gedichte

Die Darstellung von Gedicht- und Liedtexten im Fliesstext ist identisch.
Beide werden eingerückt dargestellt.

Für die bibliographische Referenz auf ein Kirchenlied (ohne Wiedergabe des
Textes) siehe [Textelemente → Lieder](../textelemente/lieder.md).

## Einzelne Zeile

```xml
<q rend="block">Errötend folgt er ihren Spuren …</q>
```

## Mehrere Zeilen

Mehrzeilige Gedicht- oder Liedtexte werden in eine Versgruppe `<lg>` mit
einzelnen Zeilen `<l>` gegliedert:

```xml
<q rend="block">
  <lg>
    <l>Was sich nie und nirgends hat begeben,</l>
    <l>Das allein veraltet nie.</l>
  </lg>
</q>
```

## Fussnote am Textende

Eine Fussnote am Ende des Gedicht- oder Liedtextes wird innerhalb des letzten
`<l>`-Elements eingefügt:

```xml
<q rend="block">
  <lg>
    <l>…</l>
    <l>Sein Wort und seine Tat dem Enkel wieder.<note xml:id="n365">V. 70-82.</note></l>
  </lg>
</q>
```

## Text am Seitenbeginn

Befindet sich der Textbeginn unmittelbar nach einem Seitenumbruch, wird
`@rend="noPipe"` am `<pb>` gesetzt — der Seitenanfang wird dann nicht am
Textfeld-Anfang, sondern nur am rechten Rand angezeigt:

```xml
<q rend="block">
  <lg>
    <l><pb rend="noPipe" xml:id="p004" ed="pga"/>Unser Leben gleicht der Reise</l>
    …
    <l>etwas, das ihm Kummer macht.<note xml:id="n01">…</note></l>
  </lg>
</q>
```
