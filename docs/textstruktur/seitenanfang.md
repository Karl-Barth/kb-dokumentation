## Seitenanfang

Seitenanfänge werden mit dem leeren Element `<pb />`(page beginning) getaggt.

## Seitenumbrüche der gedruckten Gesamtausgabe

Mit `@ed="pga"` wird angegeben, dass sich der Seitenubruch auf die gedruckte Gesamtausgabe bezieht.

Die Seitenzahl wird mit `@xml:id` angegeben: mit p (arabische Paginierung) oder pr (römische Pagnierung) und einer dreistellige Zahl.

```xml
<pb ed="pga" xml:id="pr003" /> <!-- für die Seite III -->

<pb ed="pga" xml:id="003" /> <!-- für die Seite 3 -->
```

Mit der `@xml:id` kann die Seite mit Querverweisen innerhalb der Gesamtausgabe angesteuert werden.

### Positionierung des Seitenumbruchs

Das `<pb />` muss immer innerhalb des **Textbereiches** stehen, also z.B. nicht zwischen den Absätzen (einem `</p>` und `<p>`), sondern innerhalb eine `<p>`:

```xml
<p><pb rend="noPipe" xml:id="p035" ed="pga"/> ...

<salute> <pb ed="A" n="81"/> Meine ...
```

### Seitenumbruch am Zeilenanfang
Wenn der Seitenumbruch am Beginn eines Absatzes steht oder wenn aus anderen Gründen der Seitenumbruch im Text nicht mit einem senkrechten Strich (Pipe) markiert werden soll, wird `@rend="noPipe"` hinzugefügt (am Textanfang ist dies nicht nötig). 

### Seitenumbruch am Beginn des Textes oder einer Überschrift
Am Beginn muss **immer** eine Seitenangabe für die Gesamtausgabe stehen, da sonst die Seite mit Querverweisen nicht gefunden werden kann. Die Seitenangabe ist immer 3-stellig und steht nach `<text><body><div>`:
    
```xml
<body>
  <div type="sermon">
    <pb xml:id="p039" ed="pga"/>
    <div type="opener">
      <head type="header">BLICKET AUF ZU IHM!</head>
```

Bei Seitenumbrüchen im Text, die mit dem Beginn einer Überschrift zusammenfallen wird analog `<pb />` **zwischen** das den Text umschließenden `<div>` und dem `<head>` eingetragen:

```xml
<div>
  <pb xml:id="p017" ed="pga"/>
  <head>I</head>
  <p>...</p>     
</div>
<div type="songs">
  <pb xml:id="p041" ed="pga"/>
  <head>Lieder:</head>
</div>
```

### Abstände und Worttrennung
Fällt der Seitenumbruch zwischen zwei Wörter ist je ein Leerzeichen vor und nach `<pb>` zu setzen:

```xml
... Ich <pb xml:id="p103" ed="pga" /> bitte ...
```

Fällt der Zeilenumbruch in ein Wort (Trennung) ist `@break="no"` hinzuzufügen und `<pb>` wird nicht Leerzeichen umschlossen.

```xml
... ha<pb xml:id="p037" break="no" ed="pga" />ben ...
```

Bei Trennung von "ck" wird daraus im Druck "k-k". Für die digitale Edition muss das "ck" (`c<pb/>k`) wiederherzustellen ist. <!-- TODO: abklären ob man das nicht abfangen könnte -->

## Seitenanfänge von Vorlagen der Edition

!!! note ""
    In der Regel werden nur die Seitenumbrüche gedruckter Vorlagen erfasst.


Die Vorlagen der Edition sind in der `<srcDesc>` im `<teiHeader>` erfasst. Die direkte Vorlage für die Edition enthält dort die `@xml:id="A"`. Im Text wird auf diese Source mit `@ed="A` verwiesen. Die Seitenzahl wird in `@n` (mit ganzen Zahl) erfasst:

```xml
<pb ed="A" n="3"> <!-- Seite 3 der Vorlage -->
```
