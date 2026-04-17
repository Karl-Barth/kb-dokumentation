# `<pb>` Seitenanfang

Seitenumbruch. Das @ed unterscheidet die Ausgabe (pga, A), @n die Seitenzahl.

Siehe [Textstruktur > Seitenanfang](https://dokumentation.karl-barth.ch/textstruktur/seitenanfang/)

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

## Constraints

**pb1**
:   pb1: Attribut @n in pb[@ed='A'] beginnt mit 'p'.

**pb2**
:   pb2: pb[@ed='A'] darf kein @xml:id enthalten.

**pb3**
:   pb3: Attribut @n in pb[@ed='pga'] beginnt mit 'p'.

**pb4**
:   pb4: Ein pb muss innerhalb eines Absatzes stehen oder das erste Kind eines div sein.

**pb5**
:   pb5: Einem pb[@break='no'] darf kein Leerzeichen vorangehen oder folgen.

## Beispiele

**Beispiel 1:**

```xml
<p> ... <pb n="145" ed="ed2"/>
    <!-- Seite 145 in Ausgabe "ed2" beginnt hier --> ... <pb n="283" ed="ed1"/>
    <!-- Seite 283 in Ausgabe "ed1" beginnt hier --> ... </p>
```

**Beispiel 2:**

```xml
<body>
    <pb n="1" facs="page1.png"/>
    <!-- page1.png enthält eine Abbildung der Seite;
                        der enthaltene Text ist hier kodiert -->
    <p>
      <!-- ... -->
    </p>
    <pb n="2" facs="page2.png"/>
    <!-- dasselbe gilt für Seite 2 -->
    <p>
      <!-- ... -->
    </p>
  </body>
```

## Content Model

```xml
<content>
  <empty/>
</content>
```
