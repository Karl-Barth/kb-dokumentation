# Unterschriften (`<closer>`)

## Allgemeines


## Unterschrift mit Datumsangabe
im TEI

```xml
<closer>
    <dateline rend="left">Karlsruhe und Basel, im Januar 2021.</dateline>
    <signed rend="right">Lucius Kratzert</signed>
    <signed rend="right">Peter Zocher</signed>
</closer>
```

## Unterschrift mit Grußwort ohne Datum

im TEI

```xml
<closer>
    <salute>Mit herzlichem Gruß</salute>
    <salute>Ihr</salute>
    <signed><persName ref="kbga-actors-512">Rudolf Bultmann</persName></signed>
</closer>
```

## Nur mit Unterschrift

```xml
<closer>
  <salute>Ihr</salute>
  <signed><persName ref="kbga-actors-512">R. Bultmann</persName></signed>
</closer>
```

### Unterschrift mit 2-zeiligem Grußwort

```xml
 <closer>
    <salute rendition="left">Mit ergebenem Gruße 
      <lb/>verbleibe ich hochachtungsvoll</salute>
     <signed rendition="right"><persName ref="kbga-actors-356">O. Urbach</persName></signed>
 </closer>
```

## Unterschrift mit Adresse

```xml
 <closer>
     <salute>Mit ausgezeichneter Hochachtung</salute>
     <salute>Ihr sehr ergebener</salute>
     <signed><persName ref="kbga-actors-128">Wolfgang Friedrich</persName>, stud. theol.</signed>
     <signed>1. Vorsitzender d. <orgName ref="kbga-actors-8229">Theologenschaft</orgName></signed>
     <address>
        <addrLine><placeName ref="kbga-places-41">Marburg-Lahn</placeName></addrLine>
        <addrLine>Forsthof, Ritterstr. 16</addrLine>
      </address>
  </closer>
```
