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

## Attribute

**att.global** stellt gemeinsame Attribute für alle Elemente im TEI-Kodierungsschema bereit.

**@xml:id** (optional)
:   liefert einen Identifikator für das Element, welches dieses Attribut trägt.
:   Datentyp: ID

**@n** (optional)
:   gibt eine Nummer (oder eine andere Bezeichnung) für ein Element an, die innerhalb des Dokuments nicht zwangsläufig eindeutig ist.
:   Datentyp: teidata.text

**@xml:lang** (optional)
:   gibt die Sprache des Elementinhalts durch ein Tag an, das nach BCP 47 festgelegt wird.
:   Datentyp: teidata.language

**@xml:base** (optional)
:   liefert eine Basis-URI-Referenz, mit der Anwendungen relative URI-Referenzen in absolute auflösen können.
:   Datentyp: teidata.pointer

**@xml:space** (optional, geschlossene Werteliste)
:   signalisiert die gewünschte Handhabung von Leerzeichen durch Anwendungen.
:   Datentyp: teidata.enumerated
:   `default`
:   `preserve`


**att.breaking** provides attributes to indicate whether or not the element
  concerned is considered to  mark the end of an orthographic token in the same way
  as whitespace.

**@break** (optional)
:   Datentyp: teidata.enumerated
:   `yes`
:   `no`
:   `maybe`


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


**att.edition** provides attributes identifying the source edition from which some encoded feature derives.

**@ed** (optional)
:   Datentyp: teidata.word

**@edRef** (optional)
:   Datentyp: teidata.pointer


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


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
