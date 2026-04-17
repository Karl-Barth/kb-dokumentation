# Listen (`<list>`)

```xml
<list type="simple">
  <item>Vom <hi rend="i">Lesen in der Bibel</hi>,</item>
  <item>Vom <hi rend="i">Inhalt der Bibel</hi> und</item>
  <item>Vom <hi rend="i">Glauben wie die Bibel</hi></item>
</list>
```

Listen werden mit `<list>` und `<item>` ausgezeichnet. Seitenumbrüche
(`<pb>`) müssen innerhalb eines `<item>` stehen.

## Listentypen

### Einfache Liste (`type="simple"`)

Kein führendes Aufzählungszeichen:

```xml
<list type="simple">
  <item>…</item>
  <item>…</item>
</list>
```

### Nummerierte Liste (`type="ordered"`)

Die Originalnummerierung wird in `@n` dokumentiert. Der Text wird leicht
eingerückt dargestellt:

```xml
<list type="ordered">
  <item n="1">In der Zwischenzeit … </item>
  <item n="2">Die Editionstechnik … </item>
</list>
```

### Individuell nummerierte Liste (`rend="indent"`)

Die Nummerierung mit Klammer wird in `@n` eingetragen und dem Listeneintrag
vorangestellt. Die erste Zeile steht bündig mit dem Textrand:

```xml
<list rend="indent">
  <item n="1)">Die Anschauung, …</item>
  <item n="2)">Die Anschauung, …</item>
</list>
```

### Einzug der ersten Zeile (`rend="text-indent"`)

Nur die erste Zeile jedes Eintrags ist eingezogen:

```xml
<list rend="text-indent">
  <item><hi rend="italic">1.</hi> Bildung und moralische Lebenshaltung …</item>
  <item><hi rend="italic">2.</hi> Achtung auf den Vollzug des Gesetzes!</item>
</list>
```

### Linksbündige Liste (`type="simple" rend="left"`)

```xml
<list type="simple" rend="left">
  <item><bibl corresp="kbga-songs-146">Nr. 42, Strophen 1 und 2</bibl></item>
  <item>Lektion: <ref type="can" subtype="bible" target="Ps.8">Ps. 8</ref></item>
</list>
```

## Verschachtelte Listen

Listen können geschachtelt werden, um eine Staffelung zu erzeugen:

```xml
<list type="simple">
  <item>von Ihrer Auffassung vom «Glauben»</item>
  <item>
    <list type="simple">
      <item>von Offenbarung</item>
      <item>von Heiligung</item>
    </list>
  </item>
</list>
```

## Listen innerhalb von Tabellen

Siehe [Textstruktur → Tabellen](tabellen.md).
