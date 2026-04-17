# Datumsangaben `<date>`

## Allgemeines 

Datums- und Zeitraum-Angaben werden mit `<date>` ausgezeichnet.

Ausnahmen:

- Datumsangaben in den Herausgeber-Fussnoten ohne Bezug zum Haupttext
- Datumsangaben innerhalb von `<bibl>` (wie z.B. Erscheinungsjahr)

Als Attribute werden `when`, `@from`un `@to` verwendet.

Die Datumsangaben werden mit `JJJJ`, `JJJJ-MM` oder `JJJJ-MM-DD` in den Attributen aufgelöst.

Beispiele im TEI

```xml
<date when="0333-01-05">5.Jan.333</date>

<date from="1923-01" to="1923-02">Jan./Feb. 1923</date>
```

## Unvollständige Datumsangaben
Wenn nur z.B. Tag/Monat angegeben wurde, wird das entsprechende Jahr aus dem Text ermittelt:

```xml
<date when="1922-10-05">5.10.</date>
<date when="1922-10-05">5.Okt.</date>
```

## Zeiträume

Bei nicht genau zu bestimmenden Datumsangaben werden die Attribute `from`
und `to` verwendet:

```xml
<date from="1922-10-01" to="1923-03-31">WS 1922/23</date>
<date from="1923-04-01" to="1923-09-30">SS 1923</date>
```

Für "Anfang" bzw. "Ende" eines Monats werden die **ersten bzw. letzten
fünf Tage** angegeben:

```xml
<date from="1922-01-25" to="1922-01-31">Ende Januar</date>
<date from="1922-01-01" to="1922-01-05">Anfang Januar</date>
```

## Wann nicht auszeichnen

- Innerhalb von `<bibl>` (Erscheinungsjahr, Verlagsort-Datum).
- Biographische Lebensdaten in Biogrammen (siehe
  [Textstruktur → Anmerkungen](../textstruktur/anmerkungen.md#biogramme-seg-typebio-seg-typeorg)).
- Datumsangaben in Sachfussnoten, die **keinen Bezug** zum Haupttext haben
  (z.B. Datum einer Mitteilung an den Herausgeber). Bei **inhaltlichem
  Bezug** zum Haupttext (z.B. Datum einer Bekenntnissynode) wird
  ausgezeichnet.

## Automatisierung

Die Attribute `@when`, `@from` und `@to` können weitgehend automatisiert
ausgefüllt werden, sofern die Datumsangabe mit `<date>` ausgezeichnet ist
und Jahr, Monat und/oder Tag enthält (auch mit römischen Ziffern).
Unvollständige Angaben (nur Tag/Monat) müssen manuell ergänzt werden.
