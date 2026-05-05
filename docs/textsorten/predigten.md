# Predigten (`<div type="sermon">`)

## Gesamtstruktur

```xml
<div type="sermon">
  <pb xml:id="p003" ed="pga"/>
  <div type="opener">
    <head><idno>300</idno></head>
    <dateline>…</dateline>
    <head type="event">…</head>
    <epigraph><cit><ref>…</ref><quote>…</quote></cit></epigraph>
    <salute>…</salute>
  </div>
  <div type="main">…</div>
  <div type="closer"><salute>Amen.</salute></div>
  <div type="prayer">…</div>
  <div type="songs">…</div>
</div>
```

Verpflichtend sind `opener` und `main`; alle anderen `<div>` sind optional.
Pro Datei wird online eine Seite dargestellt.

## Predigtkopf (`<div type="opener">`)

### Predigtnummer

Nummerierung durch Karl Barth. Wird oben links in Normalschrift dargestellt:

```xml
<head><idno>300</idno></head>
```

### Ort und Zeitpunkt (`<dateline>`)

Ort und Datum erscheinen rechts auf Höhe der Predigtnummer. Das Datum
muss `@when` tragen (für die Timeline). Siehe auch
[Textstruktur → Datum mit Ortsangabe](../textstruktur/dateline.md).

```xml
<dateline>
  <date when="1958-03-16">16. März 1958</date>,
  <placeName ref="kbga-places-989">Strafanstalt Basel</placeName>
</dateline>
```

Bei mehrfach gehaltenen Predigten werden die Angaben mit `<lb/>`
getrennt.

### Titel (`<head type="header">`)

Optionale Überschrift (z.B. Bd. 12), zentriert in Grossbuchstaben:

```xml
<head type="header">LEHRE UNS BEDENKEN …!</head>
```

### Anlass (`<head type="event">`)

Kirchenkalender-Anlass (Advent, Bettag usw.), zentriert unter der
Datumszeile:

```xml
<head type="event">Neujahr</head>
```

### Verweis auf Kontext (`<argument><ab>`)

Stichpunkte zum Hintergrund (aktuelle Ereignisse, Thema), kursiv und
eingerückt:

```xml
<argument>
  <ab>Ultimatum von <orgName ref="kbga-actors-8248">Österreich</orgName>
  an <orgName ref="kbga-actors-8731">Serbien</orgName></ab>
</argument>
```

### Bibelstelle (`<epigraph>`)

Die Bibelstelle und das Zitat stehen in `<epigraph><cit>`. Der Buchname
wird **ausgeschrieben** (z.B. "Matthäus" statt "Mt."). Siehe auch
[Textelemente → Bibelstellen](../textelemente/bibelstellen.md#epigraph-buchnamen-ausschreiben).

```xml
<epigraph>
  <cit>
    <ref type="can" subtype="bible" target="Ps.31.15 Ps.31.16">Psalm 31,15–16</ref>
    <quote>Ich aber, Herr, …</quote>
  </cit>
</epigraph>
```

Bei mehreren Bibelstellen wird `<epigraph>` **wiederholt** (nicht
mehrere `<cit>` in einem `<epigraph>`).

Nicht-kursive Passagen innerhalb von `<quote>` werden mit
`<hi rend="text-recte">` markiert (siehe
[Textelemente → Hervorhebungen](../textelemente/hervorhebungen.md)).

#### Nummer der Predigt zu einer Bibelstelle

Wenn Barth mehrere Predigten zur selben Stelle hält, steht die
römische Ziffer in `<span><idno>`:

```xml
<epigraph>
  <cit>
    <ref type="can" subtype="bible" target="Röm.1.16">Römer 1,16</ref>
    <span><idno>VI</idno></span>
    <quote>Ich schäme …</quote>
  </cit>
</epigraph>
```

### Ansprache (`<salute>`)

Letztes Element im `opener`:

```xml
<salute>Liebe Freunde!</salute>
```

## Predigttext (`<div type="main">`)

Hier gelten die allgemeinen Auszeichnungsregeln. Zwischenüberschriften
erzeugen wie üblich ein neues `<div>` mit `<head>` (siehe
[Textstruktur → Überschriften](../textstruktur/ueberschriften.md)).

## Abschluss (`<div type="closer">`)

"Amen" am Ende der Predigt oder des Gebets:

```xml
<div type="closer">
  <salute>Amen.</salute>
</div>
```

## Gebet (`<div type="prayer">`)

Gebete erscheinen eingerückt. Sie können vor der Ansprache (innerhalb
des `opener`) und/oder am Ende der Predigt stehen. Endet das Gebet mit
"Amen", steht ein `<div type="closer">` innerhalb des Gebets:

```xml
<div type="prayer">
  <p>Herr, unser Gott! …</p>
  <div type="closer"><salute>Amen.</salute></div>
</div>
```

## Liedliste (`<div type="songs">`)

Am Textende aufgeführte Lieder. Siehe
[Textelemente → Lieder](../textelemente/lieder.md).

```xml
<div type="songs">
  <head>Lieder:</head>
  <listBibl type="songs">
    <bibl corresp="kbga-songs-53" type="song">…</bibl>
    <bibl corresp="kbga-songs-104" type="song">…</bibl>
  </listBibl>
</div>
```

## Lesungstexte

Unterhalb der Liedliste, in einem eigenen `<div>`:

```xml
<div>
  <head>Lesungstext:</head>
  <list type="simple">
    <item><ref type="can" subtype="bible" target="Mt.25.14 Mt.25.30">Mt. 25,14–30</ref></item>
  </list>
</div>
```

## Liturgieskizzen

Wenn Liturgieskizzen aufgeführt sind, stehen sie in eigenen `<div>` mit
`<list type="simple" rend="left">`. Bei mehreren Liturgieskizzen wird
jede in ein separates `<div>` gestellt.
