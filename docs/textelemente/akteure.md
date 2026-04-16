# Akteure (`<persName>`, `<orgName>`, `<rs>`)

Für die TEI-Auszeichnung stehen drei Elemente zur Verfügung:

- `<persName>` für Personen
- `<orgName>` für Organisationen
- `<rs type="person">` für Gruppen oder nur umschriebene Personen

Namen-Konventionen, Biogramm-Regeln und Datenbank-spezifisches siehe
[Datenbank → Akteure](../datenbank/akteure.md).

Im Browser wird pro Textseite oder Fussnote nur das erste Vorkommen über das
ODD farblich hervorgehoben.

Gemeinsames ID-Schema für Personen und Organisationen: `kbga-actors-NNNN`.

## Allgemein

Kollektiv-Personen-Bezeichnungen ohne konkrete Organisationsstruktur werden
weder als Person noch als Organisation getaggt. Beispiele: "die Deutschen",
"die Italiener", "die Christen", "die deutschen Truppen",
"die deutschen Kirchenführer".

## Person `<persName>`

```xml
<persName ref="kbga-actors-313">Paulus</persName>
```

### Auszeichnung

Personen werden ausgezeichnet, wenn sie im Haupttext oder in den
Originalfussnoten genannt sind. Erscheint der vollständige Name, wird mit
**Vor- und Zuname** ausgezeichnet.

Innerhalb eines Absatzes wird eine Person mindestens **einmal** getaggt.
Bei sehr langen oder sehr kurzen Absätzen darf davon abgewichen werden.

Nicht namentlich erwähnte Personen werden nur getaggt, wenn sie inhaltlich
von Relevanz sind ("Grüsse an Ihre Frau" eher nicht, der "Führer" hingegen
schon). Im Zweifelsfall eher taggen als nicht taggen.

### Autoren in `<bibl>`

Autoren in einer `<bibl>` werden nur dann als Person ausgezeichnet und in
die Datenbank aufgenommen, wenn sie im Sinnhorizont des Haupttextes stehen
— also wenn der Autor des Haupttextes den Namen gekannt und vermutlich im
Sinn gehabt haben kann.

Autoren reiner Sekundärliteratur der Editoren erhalten **keine**
`kbga-actors-id` und erscheinen in den neuen Bänden auch nicht im Register.

### Nicht auszeichnen

- Titel vor dem Namen, sofern sie nicht unmittelbar zum Namen gehören: nicht "D. Karl Barth" oder "Dr. Karl Barth", sondern nur "Karl Barth".
- Namen innerhalb eines Buch- oder Aufsatz-**Titels**.
- Autoren von Artikeln, die erst **nach** dem vorliegenden Text erschienen sind (diese können zur Erfassung nicht zur Verfügung gestanden haben).
- Herausgebernamen in Literaturtiteln (in der Regel).
- Von einem Personennamen abgeleitete Formen, sofern sie nicht sehr eng auf die Person verweisen. So wird z.B. "Aristotelismus" nicht mit Aristoteles und "Lutheraner" oder "lutherisch" nicht als Person getaggt.

## Organisation `<orgName>`

```xml
<orgName ref="kbga-actors-9056">Heilsarmee</orgName>
```

### Auszeichnung

Als Organisation gilt z.B.:

1. Eine Firma oder ein Verlag (wenn nicht Teil einer bibliographischen Angabe).
2. Eine Institution oder ihre Abteilung (Fakultät, Direktion, Reichstag, …).
3. Ein Staat oder eine Stadt, sofern er oder sie handelt ("Frankreich erklärt den Krieg …").

### Nicht auszeichnen

- **Unbestimmte Plural-Kollektive**: "die" Deutschen, "das" Volk Israel. "Israel" nur dann, wenn sicher der heutige Staat oder (selten) das antike Nordreich gemeint ist.
- **Unbestimmte Kollektive von Organisationen**, die es als eigene Organisation nicht gibt: "die" Staaten Westeuropas, die alliierten Armeen, "die" evangelische/katholische/orthodoxe Kirche, die theologischen Fakultäten. Ist aus dem Kontext ersichtlich, dass eine bestimmte, abgrenzbare Organisation gemeint ist, wird doch ausgezeichnet.

!!! note ""
    Grundregel: Wenn nicht eindeutig eine erkennbare, abgrenzbare Institution
    gemeint ist, lieber **nicht** als Organisation auszeichnen, sondern für
    eine spätere Auszeichnung als Begriff aufsparen.

## Personen-Gruppen `<rs type="person">`

```xml
<rs type="person" ref="kbga-actors-316 kbga-actors-315">Ehepaares Pestalozzi</rs>
```

Das Element `<rs>` wird eingesetzt, wenn mehrere Personen zusammen genannt
sind ("seine Brüder", "das Ehepaar") oder wenn eine Person nur umschrieben
erscheint ("Kaiser", "Mutter").

Voraussetzung:

1. die Personen sind für den Sinn des Textes wichtig,
2. sie haben Relevanz für die Ziele der Edition, und
3. sie wurden im engeren Kontext nicht bereits mit `<persName>` ausgezeichnet.

Die IDs werden mit Leerzeichen getrennt in `@ref` eingetragen.
