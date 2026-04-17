# Fremdsprache (`<foreign>`)

```xml
<foreign xml:lang="lat">more theologorum</foreign>
```

Vom Deutschen abweichende Sprache wird mit `<foreign>` und dem Attribut
`@xml:lang` (dreistelliger Sprachcode) ausgezeichnet, sofern sich die
Passage **nicht innerhalb einer bibliografischen Angabe** (`<bibl>`)
befindet. Ausnahme: Altgriechisch wird auch in `<bibl>` ausgezeichnet,
da die Schreibweise beim automatischen Einlesen der alten Bände
fehleranfällig ist und geprüft werden muss.

Anführungszeichen um den fremdsprachigen Text werden **nicht** in das
`<foreign>` einbezogen:

```xml
… Bewegung «<foreign xml:lang="eng">For Life and Work</foreign>» veranstaltete …
```

## Sprachcodes

| Code | Sprache |
|---|---|
| `lat` | Lateinisch |
| `grc` | Altgriechisch |
| `ita` | Italienisch |
| `fre` | Französisch |
| `eng` | Englisch |
| `heb` | Hebräisch |

Bei Altgriechisch wird zusätzlich `@rend="Ell"` gesetzt:

```xml
<foreign xml:lang="grc" rend="Ell">πνεῦμα Xριστοῦ</foreign>
```
