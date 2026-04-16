# Orte (`<placeName>`)

```xml
<placeName ref="kbga-places-3">Athen</placeName>
```

Ortsnamen werden mit `<placeName>` und dem Attribut `@ref` ausgezeichnet. Über
die `kbga-places-id` werden die Daten für das Pop-up aus der Datenbank gelesen.

Namen-Konventionen, Regionskürzel und Datenbank-spezifisches siehe
[Datenbank → Orte](../datenbank/orte.md).

Die Anzeigefrequenz im Browser (Pop-up einmal pro Buchseite bzw. einmal pro
Fussnote) wird über das ODD geregelt.

## Ort oder Organisation

Ein Ort wird als `<placeName>` ausgezeichnet, wenn tatsächlich die Lokalität
gemeint ist:

- *jemand reist nach Rom*
- *jemand hat in Rom etwas gemacht*

Wird ein Ort als **handelnde Instanz** erwähnt, erfolgt die Auszeichnung als
Organisation (`<orgName>`) — siehe [Akteure](akteure.md):

- *Rom hat entschieden*

!!! note ""
    "Israel" wird nur dann als Ort ausgezeichnet, wenn sicher die geographische
    Lokalität gemeint ist; meist handelt es sich um einen Begriff, nicht um den
    Ort.

## Auszeichnung

Innerhalb eines Absatzes wird ein Ort mindestens einmal getaggt.

Wird ein Ortsname spezifiziert (z.B. "Freiburg Deutschland"), erfolgt die
Auszeichnung nur mit der ID von Freiburg. Die Spezifikation wird mit
eingeschlossen, wenn sie unmittelbar anschliesst.

Innerhalb einer **Fussnote** wird zurückhaltend getaggt — nur wenn der
Ortsname Relevanz zum Haupttext besitzt.

Ausnahmen (keine Auszeichnung als Ort):

- Ortsnamen, die **Teil eines `<orgName>`** sind. Universitäten werden als Organisation inklusive der Ortsangabe ausgezeichnet (`<orgName>Universität Basel</orgName>`).
- Ortsnamen in **bibliographischen Angaben** (`<pubPlace>`).
- Ortsnamen innerhalb von **Biogrammen** (Lebenswegstationen). Die Pop-up-Anzeige wird über das ODD ausgeblendet.
- **Abgeleitete Substantive und Adjektive** ("die Franzosen", "französisch").
