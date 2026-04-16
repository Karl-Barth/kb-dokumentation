# Akteure (`<persName>`, `<orgName>`, `<rs>`)

Regeln für die TEI-Auszeichnung von Personen (`<persName>`), Organisationen
(`<orgName>`) und Personen-Gruppen (`<rs type="person">`) im Text. Namen- und
Biogramm-Konventionen sowie Datenbank-spezifische Regeln siehe
[Datenbank → Akteure](../datenbank/akteure.md).

Allgemein wird zwischen Person und Organisation unterschieden. Über das ODD
wird im Browser nur das erste Vorkommen pro Textseite oder Fußnote farblich
hervorgehoben.

Kollektiv-Personen-Bezeichnungen, für die es keine konkrete Organisationsstruktur
gibt, werden **nicht** als Akteur oder Organisation getaggt. Beispiele:
"die Deutschen", "die Italiener", "die Christen", "die deutschen Truppen",
"die deutschen Kirchenführer".

## Person `<persName>`

### Wann zeichnen wir Personen aus

- Personen werden immer ausgezeichnet, wenn sie im Haupttext oder in den Originalfußnoten genannt werden.
- Wenn der vollständige Name erscheint, wird auch mit **Vor- und Zuname** ausgezeichnet.
- Personen werden mindestens **einmal pro Absatz** getaggt; davon wird nur bei sehr langen oder sehr kurzen Absätzen abgewichen.
- Nicht namentlich erwähnte Personen werden nur getaggt, wenn sie inhaltlich von Relevanz sind ("Grüsse an Ihre Frau" wird eher nicht getaggt, der "Führer" hingegen schon).
- Im Zweifelsfall wird eher getaggt als nicht getaggt.
- Von einem Personennamen abgeleitete Formen werden nur getaggt, wenn sie inhaltlich sehr eng auf die Person verweisen (z.B. wird "Aristotelismus" **nicht** mit Aristoteles getaggt).

Es werden keine Titel von Personen ausgezeichnet, sofern sie nicht unmittelbar
zum Namen gehören (nicht "D. Karl Barth" oder "Dr. Karl Barth", sondern nur
"Karl Barth").

Innerhalb von `<bibl>` werden die genannten Autoren nur als Person
ausgezeichnet und ggf. in die Datenbank aufgenommen, wenn die Person im
Sinnhorizont des Haupttextes vermutet werden kann, der Autor des Haupttextes
also den Namen gekannt haben kann und vermutlich an dieser Stelle auch im Sinn
gehabt haben kann. **Autoren reiner Sekundärliteratur** (Sekundärliteratur der
Editoren) werden nicht mit einer `kbga-actors-id` identifiziert und
erscheinen in den neuen Bänden auch nicht im Register.

### Wann zeichnen wir eine Person nicht aus

- Wird ein Name innerhalb eines **Titels** von einem Buch oder Aufsatz genannt, wird er **nicht** ausgezeichnet.
- Wurde die Person als Autor in einer Sachfußnote eines Artikels genannt, der nach dem Erscheinen des vorliegenden Textes veröffentlicht wurde, kann dieser nicht zur Erfassung des vorliegenden Textes zur Verfügung gestanden haben und wird nicht ausgezeichnet.
- In Literaturtiteln werden **Herausgebernamen** in der Regel nicht ausgezeichnet.
- Begriffe wie "Lutheraner" oder "lutherisch" werden nicht ausgezeichnet — nur wenn die Person direkt genannt wird.

### Die Auszeichnung im TEI

```xml
<persName ref="kbga-actors-313">Paulus</persName>
```

## Organisation `<orgName>`

### Wann zeichnen wir eine Organisation aus

Eine Organisation kann z.B. sein:

1. Eine Firma, ein Zeitungs-Verlag (wenn es nicht Teil einer bibliographischen Angabe ist).
2. Eine Institution und ebenso ihre Abteilungen (Fakultät, Direktion, Reichstag, …).
3. Ein Staat oder eine Stadt, sofern diese handelt ("Frankreich erklärt den Krieg …").

### Wann zeichnen wir nicht als Organisation aus

1. **Unbestimmte Plural-Kollektive** (z.B. "die" Deutschen, "das" Volk Israel) werden nicht als Organisationen ausgezeichnet; "Israel" z.B. nur dann, wenn _sicher_ der heutige Staat oder (ganz selten) das antike Königreich (= Nordreich) gemeint ist.
2. **Unbestimmte Kollektive von Organisationen**, die es so als eigene Organisation nicht gibt (z.B. "die" Staaten Westeuropas, die alliierten Armeen, "die" evangelische / katholische / orthodoxe Kirche — wenn nicht aus dem Kontext ersichtlich ist, dass damit doch eine ganz bestimmte, abgrenzbare gemeint ist; die theologischen Fakultäten).

Grundregel: Wenn es nicht eindeutig ist, dass eine erkennbare, als Institution
beschreibbare und abgrenzbare Organisation gemeint ist, lieber **nicht** als
Organisation auszeichnen, sondern für eine mögliche spätere Auszeichnung als
Begriff aufsparen.

### Die Auszeichnung im TEI

```xml
<orgName ref="kbga-actors-9056">Heilsarmee</orgName>
```

## Personen-Gruppen `<rs type="person">`

Die Verwendung von `<rs>` ist notwendig,

1. wenn die Personen für den Sinn des Textes wichtig sind,
2. für die Ziele der Edition Relevanz haben, und
3. wenn sie anderweitig im engeren Kontext nicht schon genannt und mit `<persName>` ausgezeichnet wurden.

Sollen im Text mehrere Personen wie "seine Brüder" oder "das Ehepaar"
ausgezeichnet werden, die keine Organisation darstellen, wird dies mit `<rs>`
ausgeführt. Die IDs der Personen werden nur mit Leerzeichen getrennt im `@ref`
eingetragen. Wird im Text nicht explizit der Name genannt, sondern z.B. nur
"Kaiser" oder "Mutter", kann dies ebenfalls mit `<rs>` ausgezeichnet werden.

### Die Auszeichnung im TEI

```xml
<rs type="person" ref="kbga-actors-316 kbga-actors-315">Ehepaares Pestalozzi</rs>
```

Gemeinsames ID-Schema für Personen und Organisationen: `kbga-actors-NNNN`.
