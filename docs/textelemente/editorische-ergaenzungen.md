# Editorische Ergänzungen (`<supplied>`)

```xml
Neutralität<supplied source="#pga">[en]</supplied>
helfen<supplied source="#dig" resp="ak">»</supplied>
```

`<supplied>` markiert Text, den ein Editor zum Originalbestand hinzugefügt
hat. `@source` unterscheidet, **welche Edition** die Ergänzung
verantwortet.

In der Webedition werden Inhalte aus der digitalen Edition
(`source="#dig"`) **grau** gerendert; ein Tooltip blendet den Hinweis
„Ergänzung der digitalen Edition" ein. `<supplied>` setzt **keine** eckigen
Klammern automatisch — wenn sie typografisch gewünscht sind, gehören sie
in den Quelltext (z.B. `<supplied source="#pga">[en]</supplied>`).

## Wann `<supplied>`, wann etwas anderes

| Fall | Auszeichnung |
|---|---|
| Print-Editor hat eine Wortvervollständigung in eckigen Klammern gesetzt | `<supplied source="#pga">…</supplied>` |
| Digitale Edition ergänzt ein im Druck fehlendes Zeichen | `<supplied source="#dig" resp="ak">…</supplied>` |
| Druckfehler korrigieren (Original sichtbar lassen) | `<choice>/<sic>/<corr>` — siehe [Korrekturen der Druckausgabe](korrekturen-der-druckausgabe.md) |
| Sachlicher Irrtum, nachträglicher Querverweis, mehrere Verweise an einer Stelle | `<note type="digital">` — siehe [Anmerkungen → Digitale Anmerkungen](../textstruktur/anmerkungen.md#digitale-anmerkungen) |

`<supplied>` ist *inline* — für einzelne Zeichen, Wörter oder kurze
Phrasen. Längere Editor-Beiträge (Kommentare, Verweis-Listen,
Erläuterungen) gehören in `<note type="digital">`.

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
    (Laravel-App) eingespeist.

## `@resp` — wer ergänzt hat

Bei `source="#dig"` ist `@resp` Pflicht und trägt das Personenkürzel
(`ak`, `sm`, …) — analog zu `<corr resp="…">` und
`<note type="digital" resp="…">`. Bei `source="#pga"` wird `@resp` in der
Regel weggelassen, weil die Print-Editoren namentlich nicht differenziert
werden.

## Beispiele

### Wortvervollständigung im Print

In einem zitierten Buchtitel hat der Print-Editor die Plural-Endung in
eckigen Klammern als optional angedeutet:

```xml
<title>Schweizer Neutralität<supplied source="#pga">[en]</supplied>
       zur Zeit des Ersten Weltkriegs.…</title>
```

Render: „Schweizer Neutralität[en] zur Zeit …" — die eckigen Klammern
stehen im Quelltext, weil sie typografisch zur Print-Konvention gehören.
Die `<supplied>`-Auszeichnung markiert sie semantisch als
Editor-Ergänzung.

### Fehlendes Satzzeichen, digital ergänzt

Im Druck fehlt ein schliessendes Anführungszeichen; in der digitalen
Edition gesetzt:

```xml
…«…den Krieg durchhalten zu helfen<supplied source="#dig" resp="ak">»</supplied>.
```

Render: das `»` wird grau dargestellt, sodass Lesende erkennen, dass das
Zeichen aus der digitalen Edition stammt.

## Abgrenzung

- **`<supplied>` vs. `<choice>/<sic>/<corr>`**: Eine Korrektur setzt
  voraus, dass im Druck *etwas Falsches* steht, das ersetzt wird.
  `<supplied>` setzt voraus, dass im Druck *etwas fehlt*, das hinzugefügt
  wird.
- **`<supplied>` vs. `<note type="digital">`**: Inline-Sigle innerhalb
  eines Satzes vs. eigenständiger Anmerkungsblock. Wenn an *einer* Stelle
  *mehrere* Verweise hängen (z.B. mehrere Briefe vom selben Tag, mehrere
  Predigten), gehört das in eine `<note type="digital">` mit der
  Verweis-Liste — nicht in mehrere `<supplied>`-Sigeln. Eine
  `<note type="digital">` kann ihrerseits `<supplied>`-Inhalte enthalten.
