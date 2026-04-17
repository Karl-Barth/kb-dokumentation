# `<lb>` Zeilenanfang

markiert den Anfang einer neuen typographischen 
    Zeile in einer bestimmten Auflage oder Version eines Textes.

Es ist Konvention, dass lb-Elemente an der Stelle im Text stehen sollen, 
      an der eine neue Zeile beginnt. Das n-Attribut enhält gegebenenfalls 
      die Nummer der Zeile oder einen ähnlichen Wert, der sich auf den Text bezieht, 
      der bis zum nächsten lb folgt, typischerweise die Nummer einer Zeile 
      auf einer Seite oder andere einschlägige Einheiten. 
    Das Element dient dazu, typographische oder paläographische Phänomene an der 
      Stelle zu beschreiben, an der sie auf dem Schriftträger sichtbar sind; 
      es sollte nicht für Struktureinheiten wie z. B. Verszeilen in Lyrik verwendet 
      werden (wofür das Element l zur Verfügung steht), außer wenn derartige 
      Struktureinheiten anders nicht markiert werden können. 
    Das type-Attribut kann verwendet werden, den Zeilenwechsel näher 
      zu beschreiben, wenn nicht die speziellen Attribute break 
      (Worttrennung), ed oder edRef (Textzeuge, in dem der 
      Zeilenwechsel vorkommt) verwendet werden können.

Siehe [Textstruktur > Zeilenumbruch](https://dokumentation.karl-barth.ch/textstruktur/zeilenumbruch/)

**Modul:** core — Kernmodule

## Kann enthalten

Leeres Element.

## Beispiele

**Beispiel 1:**

```xml
<l>Of Mans First Disobedience,<lb ed="1674"/> and<lb ed="1667"/> the Fruit</l>
<l>Of that Forbidden Tree, whose<lb ed="1667 1674"/> mortal tast</l>
<l>Brought Death into the World,<lb ed="1667"/> and all<lb ed="1674"/> our woe,</l>
```

**Beispiel 2:**

```xml
<titlePart>
    <lb/>With Additions, ne-<lb break="no"/>ver before Printed.</titlePart>
```

## Content Model

```xml
<content>
  <empty/>
</content>
```
