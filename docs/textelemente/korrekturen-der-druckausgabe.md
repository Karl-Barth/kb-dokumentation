# Korrekturen der Druckausgabe (`<choice>`, `<sic>`, `<corr>`)

```xml
<persName ref="kbga-actors-406">
  <choice>
    <sic ed="pga">Tilllich</sic>
    <corr resp="ak" type="misprint">Tillich</corr>
  </choice>
</persName>
```

Fehler in der gedruckten Gesamtausgabe werden in der digitalen Edition
nicht stillschweigend übernommen, sondern als Korrektur sichtbar gemacht.
Dafür wird `<choice>` verwendet und enthält die beiden Varianten:

- `<sic>` — der Text wie in der Vorlage (mit dem Fehler).
- `<corr>` — die korrigierte Fassung.

Das Attribut `@ed="pga"` auf `<sic>` weist darauf hin, dass sich der
fehlerhafte Text auf die gedruckte Gesamtausgabe bezieht. `<corr>` trägt
das Kürzel der korrigierenden Person im Attribut `@resp` und die Art der
Korrektur in `@type`.

## Fehlertypen (`@type`)

| Wert | Bedeutung |
|---|---|
| `misprint` | Druckfehler (Buchstabendreher, Tippfehler, falsche Schreibung) |
| `corr` | allgemeine inhaltliche Korrektur (z.B. falscher Vorname) |
| `update` | Aktualisierung (z.B. abgelaufener Link auf eine aktuelle URL) |

## Verantwortlich (`@resp`)

In `@resp` wird das Kürzel der korrigierenden Person eingetragen.

## Alternative: digitale Fussnote

Fehler können zusätzlich oder alternativ mit einer digitalen Fussnote
angemerkt werden. Siehe [Textstruktur → Anmerkungen](../textstruktur/anmerkungen.md#digitale-anmerkungen)
(`<note type="digital">`).
