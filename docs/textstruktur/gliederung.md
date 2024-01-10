# Gliederung (`<div>`)

Mit `div` werden Absätze zu einem Kapitel bzw. Textbereiche zusammengefasst. Mit der Schachtelung von `<div>` kann der Text auch hierarchiv gegliedert werden.

Wir unterscheiden die `div` mit dem Attribut `type` voneinander.

## Die Unterscheidung der Genre mit `div`

Wir benutzen `<div>` aber auch, um die einzelnen Genre, die verschieden dargestellt werden sollen, voneinander zu unterscheiden, die wir in dem **Attribut** `@type` eintragen. Sie werden nie kursiv dargestellt, die textspezifischen Unterscheidungen werden über das ODD geregelt:

| im TEI |Genre des Buches|Erklärung|
| ------ | ------ | ------ |
| `<div type="paper">`| Vorträge und kleinere Arbeiten  |mit jedem `div` innerhalb eines Files wird online eine neue "nächste Seite" erstellt|
| `<div type="letter">`|Brief|jedes File hat online eine eigene Seite|
| `<div type="sermon">`|Predigt|jedes File hat online eine eigene Seite, hier werden weitere div`s zur Textstrukturierung eingesetzt - siehe  [Predigten](sermon)|
|`<div type="chapter">`|Vorlesungsreihen|die einzelnen Kapitel einer Vorlesung. Mit jedem `div` innerhalb eines Files wird online eine neue "nächste Seite" erstellt|

## Die Unterscheidung von Texttypen innerhalb eines Buches oder auch Kapitels

| im TEI |Texttyp innerhalb des Buches |Erklärung|Darstellung|
| ------ | ------ | ------ | ------ |
| `<div type="paper">`|  Vorwort  | unabhängig von dem Buchtype, hat immer die Filenummer Band-Nr. `001` (z.B. 55001)| normal|
|  `<div type="abbreviations">`       |  Abkürzungen      | wird zukünftig online nicht dargestellt, hat immer die Filenummer Band-Nr. `002` (z.B. 55002)| normal| meist in Tabellenform|
| `<div type="abstract">`| Zusammenfassung oder Einleitung |wird zur Erläuterung vom Herausgeber angegeben |kursiv|
|`<div type="excursus">`|meist Text von einem anderen Autor oder auch nicht vorgetragene Teile einer Vorlesung| wird zur besseren Nachvollziehbarkeit des Textes angeführt | niedrigere Schrifthöhe|
| `<div type="session">`| Untergliederung einer Vorlesungsreihe nach Vortragsdatum|zur Unterteilung von Vortragsreihen innerhalb von `<div type="chapter">`|normal, das Vortragsdatum wird am rechten Seitenrand, ggf. unterhalb der Seitenangabe des Buches, angezeigt|

Insbesondere verwenden wir in den Predigten auch `<div>` um die Textbereiche zu kennzeichnen.

## Texte auf einer Seite online darstellen

Kurze Textabschnitte (`<div>`) innerhalb einer Datei können online auf einer Seite dargestellt werden, indem sie mit einem weiteren `<div>` umschlossen werden.

```xml
 <body>
      <div type="paper">
        <pb xml:id="pr007" ed="pga"/>
        <head>VORWORT</head>
        <div>(zusätzliches div für online darzustellende Seite)
          <div>
            <p>...</p>
          </div>
          <div>
            <p>...</p>
          </div>
          ...
       </div> (zusätzliches div am Ende der Seite, die online angezeigt werden soll)
       ... (ggf. weitere divs)
    </div> (div type="paper">
</body>
```
Beispiel in [19001.xml](https://kbga-pilot.karl-barth.ch/texts/19001) zu sehen.
