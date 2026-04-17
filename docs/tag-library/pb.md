# `<pb/>` (Seitenanfang)

**Modul:** Kernmodule

## Beschreibung

Seitenumbruch. Das @ed unterscheidet die Ausgabe (pga, A), @n die Seitenzahl.

## Erläuterung

Ausführliche Dokumentation:

- [Textstruktur > Seitenanfang](https://dokumentation.karl-barth.ch/textstruktur/seitenanfang/)

## Inhaltsmodell

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
