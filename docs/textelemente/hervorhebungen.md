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
| `underline` | einfache Unterstreichung, als Hervorhebung dargestellt |
| `double-underline` | doppelte Unterstreichung — Anker für editorische Anmerkungen |
| `sans-serif` | Manuskript-Unterstreichung aus einzelnen Predigtbänden; in der Webedition nicht gerendert (siehe unten) |
| `small` | verkleinert |
| `right` | rechtsbündig |
| `center` | zentriert |

Mehrere Werte können kombiniert werden, durch Leerzeichen getrennt:

```xml
<hi rend="text-small text-recte">…</hi>
<hi rend="sans-serif italic">…</hi>
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

## Unterstreichungen im Manuskript

`<hi rend="underline">` bezeichnet einfache Unterstreichungen im Manuskript
(vorwiegend in Bd. 18, 49, 57). Urheber und Zeitpunkt sind nicht immer
eindeutig; sie werden in der Webedition als Hervorhebung dargestellt.

`<hi rend="double-underline">` markiert in den «Bemerkungen zum Betheler
Bekenntnis» (Bd. 49) doppelte Unterstreichungen, die als Anker für
editorische Anmerkungen dienen.

```xml
<hi rend="underline">Alle Lehre der Kirche</hi>
<hi rend="double-underline">Liebe</hi>
```

## Abweichung von der gedruckten Ausgabe: `sans-serif`

In den Predigtbänden **Bd. 37, 39, 42, 44** und im Vorträge-Band **Bd. 48**
hat Barth Unterstreichungen im Manuskript mit Blaustift, Farbstift oder als
doppelte Bleistiftlinie angebracht. Die gedruckte Ausgabe kennzeichnet diese
durch eine abweichende Schrift (Helvetica); für die Kombination mit einer
Tintenunterstreichung (bzw. in Bd. 48 das Zusammentreffen einer gedanklichen
mit einer rhetorischen Markierung) wird «kursive Helvetica» gesetzt.

In den XML-Daten sind diese Fälle einheitlich mit `<hi rend="sans-serif">`
bzw. `<hi rend="sans-serif italic">` ausgezeichnet. **Die Webedition
ignoriert `sans-serif`** — das Tag bleibt als Spur der Manuskript-Markierung
erhalten, hat aber keinen visuellen Effekt. Nur das explizite `italic` in
`sans-serif italic` wird als Kursivsatz gerendert.

Die übrigen Predigtbände — sowohl die älteren als auch die neueren — haben
entsprechende Manuskript-Unterstreichungen gar nicht gesondert ausgezeichnet.
Die Bedeutung solcher Unterstreichungen (Blaustift, Farbstift, Doppelstrich)
ist in den meisten Fällen unklar, da Urheber und Zeitpunkt nicht zuverlässig
bestimmbar sind. Die Vereinheitlichung stellt die Konsistenz der digitalen
Gesamtausgabe her, ohne eine Differenzierung zu suggerieren, die sich nicht
rekonstruieren lässt. Die Original-Darstellung der Helvetica-Auszeichnung
bleibt im **PDF der gedruckten Ausgabe** einsehbar.

## Kombinationen

Mehrere Werte in einem `@rend` werden mit Leerzeichen getrennt. Reihenfolge
ist nicht bedeutungstragend; zur besseren Lesbarkeit kann die typografische
Hauptdarstellung zuletzt stehen:

```xml
<hi rend="text-small text-recte">…</hi>   <!-- klein + senkrecht -->
<hi rend="underline italic">…</hi>        <!-- unterstrichen + kursiv -->
<hi rend="sans-serif italic">…</hi>       <!-- Manuskript-Spur + kursiv -->
```
