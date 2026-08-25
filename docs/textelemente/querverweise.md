# Querverweise und Links (`<ref>`)

## Übersicht der Verweis-Typen

| Typ | TEI | Ziel |
|---|---|---|
| Bibelstelle | `<ref type="can" subtype="bible" target="…">` | Pop-up mit Bibeltext |
| Innerhalb der KBGA | `<ref type="pub" target="…">` | Seite/Fussnote eines publizierten Bandes |
| Noch nicht publizierter Band | `<ref type="pub-" target="…">` | wie `pub`, aber Band noch nicht online |
| Innerhalb desselben Textes | `<ref type="cross" target="…">` | Anker im selben Text/Band |
| Karl Barth-Archiv | `<ref type="kba-objects-id" target="…">` | Objekt im Karl Barth-Archiv |
| KBA-Signatur bei der Erfassung | `<idno type="kba-objects-identifier">` | wird in die `<ref>`-Form umgewandelt |
| Externe URL | `<ref type="url" target="https://…">` | externer Link (neuer Tab) |
| Vorlage | `<ref corresp="B">Mskr.</ref>` | Pop-up mit Vorlagen-Info aus teiHeader |
| Archiv ohne Zugang | `<bibl type="archival">` | keine Darstellung (nur Metadaten) |

Für Bibelstellen siehe [Textelemente → Bibelstellen](bibelstellen.md).
Für Vorlagen-Verweise in textkritischen Anmerkungen siehe
[Textstruktur → Anmerkungen](../textstruktur/anmerkungen.md#verweis-auf-vorlagen).

## Querverweise innerhalb der KBGA (`type="pub"`)

Jedes Ziel wird über die **Bandnummer** (zweistellig) und die
**Seitenzahl** (dreistellig) oder die **Filenummer** adressiert.

### Auf eine bestimmte Seite

Die Seitenangabe wird zweimal eingetragen: einmal für die Datenbanksuche
nach dem richtigen File, einmal für den Browser-Anker:

```xml
<ref type="pub" target="../volume/04/p306#p306">S. 306</ref>
```

### Auf eine Seite und Fussnote

```xml
<ref type="pub" target="../volume/01/p299#fn_n22">S. 299 Anm. 22</ref>
```

### Mit Filenummer (empfohlen bei kurzen Texten)

Bei kurzen Texten (Briefen, Predigten) können mehrere Files auf derselben
Buchseite beginnen. Die Filenummer macht den Verweis eindeutig:

```xml
<ref type="pub" target="1005">Nr. 3</ref>
<ref type="pub" target="1005#fn_n15">Nr. 3, Anm. 15</ref>
<ref type="pub" target="1001#pr006">S. VI</ref>
```

### Auf einen ganzen Band (Inhaltsseite)

```xml
<ref type="pub" target="../texts?facet-volume=55">Vorträge und kleinere Arbeiten 1935–1937</ref>
```

### Vorwort

Das Vorwort hat immer die Filenummer `001`. Seitenangaben im Vorwort
beginnen mit `pr` (römische Paginierung):

```xml
<ref type="pub" target="55001#pr006">S. VI</ref>
```

### Fussnote im gleichen File

```xml
<ref type="pub" target="#fn_n18">Anm. 18</ref>
```

### Seite in einem durch `<div>` geteilten File

Kommt dieselbe Seitenzahl in zwei `<div>` vor, wird ein `<anchor>` auf
der zweiten Seite gesetzt und mit der Filenummer + `?id=` angesprungen:

```xml
<anchor xml:id="p306b"/>
<!-- … -->
<ref type="pub" target="40006?id=p306b">S. 306f.</ref>
```

## Noch nicht publizierte Bände (`type="pub-"`)

Für Bände, die noch nicht online verfügbar sind, wird `type="pub-"`
verwendet. Sobald der Band publiziert ist, wird `pub-` durch `pub` ersetzt.

## Querverweise innerhalb desselben Textes (`type="cross"`)

Für Verweise innerhalb desselben Textes oder Bandes wird `<ref type="cross">`
mit einem `<anchor>`-Ziel verwendet:

```xml
<anchor xml:id="kbga-texts-55012_1"/>
<!-- … -->
<ref type="cross" target="kbga-texts-55012_1">S. X</ref>
```

Von-bis-Verweise benennen Anfangs- und End-Anker im `@target`:

```xml
<ref type="cross" target="kbga-texts-55012_2a kbga-texts-55012_2b">S. X–Y</ref>
```

## Links ins Karl Barth-Archiv

### Bevorzugte Form

Verweise ins Karl Barth-Archiv werden mit `<ref type="kba-objects-id">` und der
**Objekt-ID** im `@target` ausgezeichnet — unabhängig davon, ob die Signatur im
Text steht oder nicht:

```xml
<ref type="kba-objects-id" target="23143">KBA 9234.23</ref>
<ref type="kba-objects-id" target="11854">Brief im Karl Barth-Archiv</ref>
```

Der Elementinhalt bleibt der Text der Edition: die Signatur, wenn sie im Text
steht, sonst eine Umschreibung («Brief im Karl Barth-Archiv»,
«Taschenkalender»). Die Objekt-ID ist stabil und überlebt eine Umsignierung im
Archiv.

### Erfassung mit `<idno>`

Steht die Signatur im Text und ist die Objekt-ID nicht zur Hand, darf bei der
Erfassung `<idno>` gesetzt werden:

```xml
<idno type="kba-objects-identifier">KBA 9234.303</idno>
```

Diese Form wird regelmässig automatisch in die bevorzugte `<ref>`-Form
überführt; der Elementinhalt bleibt dabei unverändert. `<idno>` kann kein
`@target` tragen — die RNG lässt darauf nur `@xml:id` und `@type` zu —, die
Auflösung läuft deshalb über den Signatur-String und setzt voraus, dass die
Signatur unverändert im Archiv verzeichnet ist.

Nicht auflösbar und damit dauerhaft als `<idno>` stehen bleiben Signaturen, die
im Archiv kein eigenes Objekt haben. Das betrifft vor allem editorische
Unterscheidungen physisch getrennter Exemplare innerhalb einer
Verzeichnungseinheit, etwa `KBA 11109.1` und `KBA 11109.2` für zwei
Durchschläge desselben Dossiers `KBA 11109`.

## Externe Links (`type="url"`)

Links auf externe Webseiten beginnen mit `https://`:

```xml
<ref type="url" target="https://www.jacomet.ch/…">www.andijacomet.ch</ref>
```

## Archiv-Verweise (`<bibl type="archival">`)

Verweise auf Archive, zu denen kein digitaler Zugang besteht, werden mit
`<bibl type="archival">` erfasst. Sie werden im Browser nicht dargestellt:

```xml
<bibl type="archival">UB Tübingen, Mn 2/2261</bibl>
```
