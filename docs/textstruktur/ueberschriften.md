# Überschriften

## Einleitung

Überschriften werden mit `<head>` ausgezeichnet. Da in der gedruckten Ausgabe die Überschriften je nach Ort und Form, d.h. Abstand zum Text und Rand, kursiv oder normaler Text, unterschiedlich dargestellt wird, reicht es nicht, es dabei zu belassen.

Es wurde versucht, über die Regeln im ODD der Darstellung im gedruckten Buch möglichst nahe zu kommen, ohne viel im TEI einfügen zu müssen.

Auch muss beachtet werden, dass nach einem Absatz ein `<div>` benötigt wird, um ein `<head>` einzubauen, d.h. ein `<head>` kann nicht direkt einem Absatz `<p>` folgen.

!!! note ""

    Ziel ist es, möglichst viel über die Regeln im ODD abzufangen und 
    **möglichst im TEI** spezifizieren zu müssen. Die Überschriften sollen 
    möglichst vereinheitlicht werden.

## Überschriften

### Erste Überschrift
Die Struktur ist hier immer `text/body/div` und innerhalb des `<div>` dann `<pb>` gefolgt von `<head>` ohne weiteres Attribut. <!--Die Seitenzahl wird dann über das ODD am rechten Seitenrand dargestellt.-->

```xml
<text>
    <body>
      <div type="paper">
        <pb xml:id="pr007" ed="pga"/>
        <head>VORWORT ZUR 2. AUFLAGE</head>
        <p>...
```

### Weitere Überschriften
Um die Hierarchie eines Textes zu rekonstruieren werden in TEI `<div>` geschachtelt. Jedes `<div>` kann dabei ein eigenes `<head>` enthalten:

```xml
<div>
    <head>Ebene 1</head>
    <p>...</p>
    ...
    <div>
        <head>Ebene 2</head>
    </div>
</div>
```


## Untertitel

Unterüberschriften, die sich auf den selben Abschnitt wie die Hauptüberschrift beziehen – also Untertitel –, werden mit `@type="sub"` spezifiziert. 

```xml
<div type="paper"> 
      <pb xml:id="pr009" ed="pga"/>
      <head>VORWORT</head>
      <head type="sub"><hi rend="i">1.) Dank an Hermann Schmidt</hi></head>
      <p>...
```

## Abweichende Formatierungen

Standardmässig werden Unterüberschriften kursiv und zentriert dargestellt. Abweichende Formatierungen können über `@rend` spezifiziert werden. 

Werte (bisher verwendet)

- "left"
- "head-kursiv" (identisch wie italic?)
- "italic"
- "larger-text" (bis jetzt nur einmal verwendet, evtl. rausschmeissen?)

## Texte ohne Überschrift

siehe

- Predigten  
- Briefe
