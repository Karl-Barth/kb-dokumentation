# Editorische Ergänzungen (`<supplied>`)

```xml
<supplied source="#pga">uder</supplied>
<supplied source="#dig" resp="ak">.</supplied>
```

`<supplied>` markiert Text, den ein Editor zum Originalbestand hinzugefügt
hat. In der Webedition werden die Inhalte in eckigen Klammern dargestellt;
`@source` unterscheidet, **welche Edition** die Ergänzung verantwortet.

## Wann `<supplied>`, wann etwas anderes

| Fall | Auszeichnung |
|---|---|
| Print-Editor hat im Buch eckige Klammern gesetzt (Wortvervollständigung, recherchiertes Datum, Sprecherangabe) | `<supplied source="#pga">…</supplied>` |
| Digitale Edition ergänzt ein im Druck fehlendes Satzzeichen | `<supplied source="#dig" resp="ak">.</supplied>` |
| Digitale Edition setzt einen Verweis-Anker für Archiv- oder Querverweise, der im Druck keinen Anker hatte | `<supplied source="#dig" resp="sm"><ref …>Brief</ref></supplied>` |
| Druckfehler korrigieren (Original sichtbar lassen) | `<choice>/<sic>/<corr>` — siehe [Korrekturen der Druckausgabe](korrekturen-der-druckausgabe.md) |
| Sachlicher Irrtum oder nachträglicher Querverweis (Block-Anmerkung) | `<note type="digital">` — siehe [Anmerkungen → Digitale Anmerkungen](../textstruktur/anmerkungen.md#digitale-anmerkungen) |

`<supplied>` ist *inline* — für einzelne Zeichen, Wörter oder kurze Phrasen.
Längere Editor-Beiträge (Verweis-Listen, Erläuterungen) gehören in
`<note type="digital">`.

## `@source` — woher die Ergänzung stammt

| Wert | Bedeutung |
|---|---|
| `#pga` | aus der gedruckten Karl Barth-Gesamtausgabe (Print-Editor hat ergänzt) |
| `#dig` | aus der digitalen Edition (wir haben ergänzt) |

Die Werte zeigen auf `<bibl>`-Einträge im `<sourceDesc>` des `<teiHeader>`:

```xml
<sourceDesc>
  <bibl xml:id="pga" type="edition">Karl Barth-Gesamtausgabe (gedruckt).</bibl>
  <bibl xml:id="dig" type="edition">Karl Barth-Gesamtausgabe, digitale Edition.</bibl>
  …
</sourceDesc>
```

!!! note "teiHeader wird aus der Datenbank befüllt"
    Die `<bibl xml:id="pga">` und `<bibl xml:id="dig">` werden nicht direkt
    in den `vol-*/*.xml`-Dateien gepflegt, sondern über die Meta-Datenbank
    (Laravel-App) eingespeist. Eine Anpassung in den Quelldateien ist
    deshalb nicht nötig.

Im Render werden beide Varianten in eckigen Klammern dargestellt; digitale
Ergänzungen (`#dig`) zusätzlich abgesetzt (graue Schrift), damit Lesende sie
von den Print-Klammern unterscheiden können.

## `@resp` — wer ergänzt hat

Bei `source="#dig"` wird `@resp` mit dem Personenkürzel gesetzt
(`ak`, `sm`, …) — analog zu `<corr resp="…">` und
`<note type="digital" resp="…">`. Bei `source="#pga"` ist `@resp` in der
Regel weggelassen, weil die Print-Editoren namentlich nicht differenziert
werden.

## Beispiele

### Wortvervollständigung im Print

Der Print-Editor hat im Original eine abgekürzte Form expandiert:

```xml
…lieber Br<supplied source="#pga">uder</supplied>…
```

### Fehlendes Satzzeichen, digital ergänzt

Im Druck fehlt ein schliessendes Anführungszeichen; in der digitalen
Edition gesetzt:

```xml
…«…den Krieg durchhalten zu helfen<supplied source="#dig" resp="ak">»</supplied>.
```

### Verweis-Anker, der im Druck fehlt

Eine Fussnote der digitalen Edition referenziert einen weiteren Brief vom
selben Tag, für den im Drucktext kein Anker existiert:

```xml
…am 11.9.1933 an D. Bonhoeffer (…) und an
<supplied source="#dig" resp="sm">
  <ref type="kba-objects-id" target="22166">Brief</ref>
</supplied>
Renatus Hupfeld, …
```

Der Sigle-Text („Brief") steht in eckigen Klammern und ist gleichzeitig
Klick-Anker auf das Archiv-Objekt.

## Abgrenzung

- **`<supplied>` vs. `<choice>/<sic>/<corr>`**: Eine Korrektur setzt
  voraus, dass im Druck *etwas Falsches* steht, das ersetzt wird.
  `<supplied>` setzt voraus, dass im Druck *etwas fehlt*, das hinzugefügt
  wird.
- **`<supplied>` vs. `<note type="digital">`**: Inline-Sigle innerhalb
  eines Satzes vs. eigenständiger Anmerkungsblock. Eine
  `<note type="digital">` kann ihrerseits `<supplied>`-Inhalte enthalten.
