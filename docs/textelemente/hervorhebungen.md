# Hervorhebungen (`<hi>`)

```xml
<hi rend="italic">Gott</hi>
```

Abweichende typografische Darstellungen eines Textabschnitts werden mit
`<hi>` und dem Attribut `@rend` ausgezeichnet. Der Wert von `@rend` steuert,
wie der Text dargestellt wird.

Vorhandene Kursivierungen und andere Hervorhebungen im Haupttext und in den
Originalfussnoten werden **nicht verändert**, ausser sie weichen von der
gedruckten Ausgabe ab.

## Verwendete `@rend`-Werte

| `@rend` | Darstellung |
|---|---|
| `italic` | kursiv |
| `text-recte` | senkrecht (normal), innerhalb eines kursiven Abschnitts |
| `sup` | hochgestellt |
| `sub` | tiefgestellt |
| `top` | Zähler eines Inline-Bruchs |
| `buttom` | Nenner eines Inline-Bruchs |
| `bold` | fett |
| `smallCaps` | Kapitälchen |
| `spaced` | gesperrt |
| `underlined-later` | nachträgliche Unterstreichung im Manuskript |
| `underline` | einfache Unterstreichung |
| `small` | verkleinert |
| `right` | rechtsbündig |
| `center` | zentriert |

Mehrere Werte können kombiniert werden, durch Leerzeichen getrennt:

```xml
<hi rend="text-small text-recte">…</hi>
<hi rend="underline italic">…</hi>
<hi rend="bold italic">…</hi>
```

## Kursiv vs. senkrecht

Innerhalb eines Abschnitts, der durch das umschliessende `<div>` bereits
kursiv dargestellt wird (z.B. `<div type="abstract">` für Einleitungen),
wird ein hervorgehobener senkrechter Abschnitt mit `<hi rend="text-recte">`
markiert. Das hebt ihn vom kursiven Kontext ab.

```xml
<div type="abstract">
  <p><hi rend="text-recte">Ich bitte</hi> … </p>
</div>
```

## Hochstellung (`sup`)

Für hochgestellte Zeichen, insbesondere Auflagezahlen in bibliografischen
Angaben. Zwischen Erscheinungsjahr und Auflagezahl steht kein Leerzeichen:

```xml
1849<hi rend="sup">3</hi>
```

Siehe [Textelemente → Literatur](literatur.md).

## Inline-Brüche (`top` / `buttom`)

Für typografisch gesetzte Brüche im Fliesstext (halbe Stunden, Anteile,
Auflagenspannen) werden die Werte `top` (Zähler) und `buttom` (Nenner) als
Paar verwendet. Beide werden auf etwa 50 % der Schriftgrösse skaliert und
entsprechend hoch- bzw. tiefgestellt dargestellt. `top`/`buttom` sind von
`sup`/`sub` abzugrenzen: `sup` steht für Auflagezahlen und andere
hochgestellte Zeichen in 75 % Schriftgrösse, `sub` für tiefgestellte Zeichen;
`top`/`buttom` hingegen bilden zusammen mit einem Schrägstrich einen Bruch.

```xml
1<hi rend="top">1</hi>/<hi rend="buttom">2</hi>          <!-- 1½ -->
<hi rend="top">1</hi>/<hi rend="buttom">2</hi>8 Uhr     <!-- ½8 Uhr (halb acht) -->
2<hi rend="top">1</hi>/<hi rend="buttom">2</hi>te       <!-- 2½te Internationale -->
```

Der Schreibfehler `buttom` (statt `bottom`) wurde aus historischen Gründen
beibehalten; eine Umbenennung würde die Rendering-Regel in der ODD
voraussetzen.

## Manuskript-Unterstreichungen

In einigen Bänden werden Unterstreichungen, die im Manuskript nachträglich
angebracht wurden (in der Regel mit Tinte oder Blaustift), mit
`<hi rend="underlined-later">` ausgezeichnet. In der digitalen Edition werden
sie einheitlich als Hervorhebung dargestellt; die ursprüngliche Unterscheidung
von Tinte und Blaustift der gedruckten Ausgabe wird nicht reproduziert.

## Kombinationen

Mehrere Werte in einem `@rend` werden mit Leerzeichen getrennt. Reihenfolge
ist nicht bedeutungstragend; zur besseren Lesbarkeit kann die typografische
Hauptdarstellung zuletzt stehen:

```xml
<hi rend="text-small text-recte">…</hi>   <!-- klein + senkrecht -->
<hi rend="underline italic">…</hi>        <!-- unterstrichen + kursiv -->
<hi rend="underlined-later italic">…</hi>
```
