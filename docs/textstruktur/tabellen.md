# Tabellen (`<table>`)

```xml
<table>
  <row>
    <cell>…</cell>
    <cell>…</cell>
  </row>
  <row>
    <cell>…</cell>
    <cell>…</cell>
  </row>
</table>
```

Tabellen werden mit `<table>`, `<row>` und `<cell>` ausgezeichnet. Die
Anzahl der Spalten wird automatisch berechnet; jede Zeile muss dieselbe
Anzahl Zellen haben (leere Zellen als `<cell/>`). Seitenumbrüche und
Text müssen innerhalb von `<cell>` stehen.

Wird in einer Zelle mit einem Attribut eine Formatierung angegeben, gilt
diese automatisch für alle Zellen in derselben Spaltenposition.

## Spaltenbreite

### Gleichbreite Spalten

Mit `@rend="100p"` auf `<table>` und `@rend="width(50%)"` auf der ersten
Zelle:

```xml
<table rend="100p">
  <row>
    <cell rend="width(50%)"> [Vortragsmanuskript]</cell>
    <cell/>
  </row>
  <row>
    <cell>…</cell>
    <cell>…</cell>
  </row>
</table>
```

### Unterschiedliche Spaltenbreite

Die Breite der ersten Spalte wird prozentual angegeben, die restlichen
Spalten teilen sich den verbleibenden Platz:

```xml
<table>
  <row>
    <cell rend="width10%">«1933</cell>
    <cell>Bejahung des Nationalsozialismus …</cell>
  </row>
</table>
```

## Zellen über mehrere Spalten

Mit `@cols` wird angegeben, über wie viele Spalten eine Zelle reicht:

```xml
<cell cols="2">Text über zwei Spalten</cell>
```

## Kombination von Liste und Tabelle

Wenn innerhalb einer Liste Wörter untereinander stehen sollen, kann statt
einer `<list>` eine `<table>` verwendet werden. Umgekehrt können `<list>`-
Elemente innerhalb einer `<cell>` stehen. Siehe auch
[Textstruktur → Listen](listen.md).

```xml
<table rend="margin-left">
  <row>
    <cell>Evangelium zu <hi rend="i">verfälschen</hi>:</cell>
    <cell>deutschchristliche Kirche</cell>
  </row>
</table>
```
