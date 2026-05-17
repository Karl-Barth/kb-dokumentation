# Bibelstellen (`<ref type="can" subtype="bible">`)

```xml
<ref type="can" subtype="bible" target="Mt.15.27">Mt. 15,27</ref>
```

Bibelstellen werden mit `<ref>` ausgezeichnet. Die Attribute `@type="can"` und
`@subtype="bible"` kennzeichnen die Angabe als kanonische Bibelreferenz; das
Attribut `@target` enthält die Stelle in maschinenlesbarer Form und wird zur
Verknüpfung mit dem Bibeltext verwendet.

Die verwendeten Buchabkürzungen und die kanonische Reihenfolge siehe
[Bibelbücher](../bibel.md).

## Format des `@target`

Im `@target` steht die Stelle **ohne Leerzeichen**, mit Punkten als Trenner:

```
Buchabkürzung.Kapitel.Vers
```

Im Anzeigetext (zwischen den Tags) steht die Stelle lesbar formatiert: nach
der Buchabkürzung ein Leerzeichen, zwischen Kapitel und Vers ein Komma.

| im Text | im `@target` |
|---|---|
| `Mt. 15,27` | `Mt.15.27` |
| `Röm. 5,12` | `Röm.5.12` |
| `Apk. 22,7` | `Apk.22.7` |

### Vorangestellte Zahl bei mehrgliedrigen Büchern

Bei Büchern mit vorangestellter Zahl (1./2. Korinther, 1./2./3. Johannes,
1./2. Petrus usw.) wird die Zahl im Anzeigetext und im `@target` jeweils
mit einem Punkt an die Abkürzung angehängt:

```xml
<ref type="can" subtype="bible" target="1.Kor.8.6">1.Kor. 8,6</ref>
```

### Einkapitel-Bücher

Sechs Bücher der Lutherbibel 1912 haben nur ein Kapitel:

| Abkürzung | Buch |
|---|---|
| `Obd` | Obadja |
| `Phlm` | Philemon |
| `2.Joh` | 2. Johannesbrief |
| `3.Joh` | 3. Johannesbrief |
| `Jud` | Judasbrief |
| `Geb.Man` | Gebet Manasses (Apokryphen) |

Sie werden im Anzeigetext oft ohne Kapitelangabe zitiert ("Jud. 9",
"2.Joh. 7"). Im `@target` muss aber **immer** ein Pseudo-Kapitel `1`
zwischen Buch und Vers stehen, weil der Bibeltext-Pop-up sonst nicht
aufgelöst werden kann:

```xml
<!-- richtig -->
<ref type="can" subtype="bible" target="Jud.1.9">Jud. 9</ref>
<ref type="can" subtype="bible" target="2.Joh.1.7">2.Joh. 7</ref>

<!-- falsch — Pop-up rendert als "Verse reference not found" -->
<ref type="can" subtype="bible" target="Jud.9">Jud. 9</ref>
```

## Versbereiche und Wiederholungen

Bezeichnet die Angabe mehr als einen Vers, enthält `@target` den **ersten**
und den **letzten** Vers des Bereichs, getrennt durch ein Leerzeichen.

### `f.` — Editor: Folgevers; Barth: Perikope

Die Bedeutung von `f.` hängt davon ab, wer die Bibelstelle eingefügt hat —
das lässt sich an den Klammern erkennen:

| Schreibweise | Urheber | Bedeutung | `@target` |
|---|---|---|---|
| `[Lk. 15,22f.]` in eckigen Klammern | Editor | Vers 22 und 23 | `Lk.15.22 Lk.15.23` |
| sonst (`(Lk. 15,22f.)` oder ohne Klammern) | Barth | Perikope ab Vers 22 | letzter Vers der Perikope (manuell nachgeschlagen) |

```xml
<!-- Editor-Ergänzung: Folgevers -->
[vgl. <ref type="can" subtype="bible" target="Lk.15.22 Lk.15.23">Lk. 15,22f.</ref>]

<!-- Barth: Perikope (Endvers nachgeschlagen) -->
(<ref type="can" subtype="bible" target="Röm.12.1 Röm.12.8">Röm. 12,1f.</ref>)
```

### `ff.` — bis zum Ende der Perikope

Die Angabe "Lk. 10,30ff." meint die ganze Perikope ab Vers 30, unabhängig
vom Klammer-Kontext. Für `@target` wird der **letzte Vers der Perikope**
gesucht; der Bibeltext öffnet sich im Pop-up dann im angegebenen Bereich.

```xml
<ref type="can" subtype="bible" target="Lk.10.30 Lk.10.37">Lk. 10,30ff.</ref>
```

Das Ende der Perikope (in der Regel durch eine Zwischenüberschrift markiert)
lässt sich z.B. über
[bibleserver.com](https://www.bibleserver.com/LUT/Lukas10%2C30) nachschlagen.

### Bereich mit Gedankenstrich

Steht ein Gedankenstrich in der Angabe ("Röm. 5,12–21"), werden Anfang und
Ende als zwei Einträge in `@target` notiert:

```xml
<ref type="can" subtype="bible" target="Röm.5.12 Röm.5.21">Röm. 5,12–21</ref>
```

!!! note ""
    Enthält der Anzeigetext ein `f.`, `ff.` oder einen Gedankenstrich und
    `@target` nur einen einzelnen Vers, ist die Auszeichnung unvollständig
    und muss korrigiert werden.

## Zwei einzelne Verse mit Punkt-Trennung

Folgt auf einen Vers ein weiterer Vers in demselben Kapitel, getrennt durch
einen Punkt ("Apk. 22,7.12"), bezeichnet die Angabe **zwei einzelne** Verse
(nicht einen Bereich). Sie wird daher in **zwei getrennte** `<ref>`-Elemente
aufgeteilt; der Punkt bleibt als normaler Text zwischen den beiden Elementen:

```xml
<ref type="can" subtype="bible" target="Apk.22.7">Apk. 22,7</ref>.<ref type="can" subtype="bible" target="Apk.22.12">12</ref>
```

Im Browser öffnet der interessierte Leser nacheinander zwei Pop-ups.

## Mehrere Kapitel

Nur **ein einzelnes** Kapitel wird ausgezeichnet. Angaben wie
"Röm. 13,8 / Röm. 14,2" können als zwei getrennte `<ref>`-Elemente oder als
ein `<ref>` mit zwei space-getrennten Einträgen im `@target` erfasst werden:

```xml
<ref type="can" subtype="bible" target="Röm.13.8 Röm.14.2">Röm. 13,8; 14,2</ref>
```

Pauschalangaben ohne Versnummer ("Römer 3–4") werden **nicht** ausgezeichnet.

## Epigraph — Buchnamen ausschreiben

Innerhalb eines `<epigraph>` (Motto-Zitat an einem Textanfang, insbesondere
in Predigten) wird der Buchname im Anzeigetext **ausgeschrieben**, damit er
im gedruckten und im Online-Text nicht als Abkürzung erscheint. Im `@target`
bleibt die Abkürzung bestehen:

```xml
<ref type="can" subtype="bible" target="Lk.1.53">Lukas 1,53</ref>
```

## Nicht innerhalb `<bibl>`

Bibelstellen werden **nicht** innerhalb einer Literaturangabe (`<bibl>`)
ausgezeichnet — auch wenn der Werktitel oder ein Klammer-Zusatz eine
Bibelstelle nennt. Der zugehörige Eintrag wird über die
Literatur-Datenbank verlinkt; ein zusätzliches Bibel-Pop-up würde den
Lesefluss stören. Vgl. [Literatur](literatur.md).

```xml
<!-- richtig: keine <ref>-Auszeichnung der Bibelstelle im Titel -->
<bibl corresp="kbga-bibls-2050">
  Eine akademische Vorlesung über 1.Kor. 15
</bibl>
```

## Bibel-Quelle

Der in den Pop-ups angezeigte Bibeltext stammt aus der Lutherübersetzung 1912
der Deutschen Bibelgesellschaft (USX 3.0).

Das Bibelstellen-Register wird nicht in der Metadatenbank erfasst, sondern
direkt aus den `<ref>`-Elementen der TEI-Texte generiert.
