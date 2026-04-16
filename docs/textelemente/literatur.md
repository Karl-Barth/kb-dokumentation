# Literatur (`<bibl>`)

```xml
<bibl corresp="kbga-bibls-647">
  <persName ref="kbga-actors-136">J. W. von Goethe</persName>, 
  <hi rend="i">Faust I</hi>, V. 3460f. (Marthens Garten)
</bibl>
```

Bibliografische Angaben werden mit `<bibl>` ausgezeichnet. Das Attribut
`@corresp="kbga-bibls-NNNN"` verweist auf den Eintrag in der Literatur-
Datenbank, in der die detaillierten bibliografischen Felder erfasst sind
(Autor, Titel, Verlag, Erscheinungsjahr usw.).

Datenbank-spezifisches (Typen, Titelfelder, Auflagen, Filme, Archivbestände)
siehe [Datenbank → Literatur](../datenbank/literatur.md).

## Wann mit `<bibl>` ausgezeichnet wird

### Im Haupttext

Jede Literaturangabe wird mit `<bibl>` umschlossen — ausser die gleiche Angabe
wird in der **direkt folgenden Fussnote** wiederholt. In diesem Fall
unterbricht die Auszeichnung den Lesefluss unnötig; das ODD zeigt identische
Referenzen pro Buchseite nur einmal als Pop-up.

### In Fussnoten

In Sach- und Originalfussnoten wird jede Literaturangabe immer mit `<bibl>`
ausgezeichnet. Das ODD zeigt identische Referenzen pro Fussnote nur einmal
als Pop-up.

### Kurze Referenzen

Abkürzungen mit Seitenzahl (z.B. `a.a.O. Seitenzahl`) werden vollständig mit
`<bibl>` ausgezeichnet:

```xml
<note xml:id="n32"><bibl corresp="kbga-bibls-2971">Z 2,606,14-607,14.</bibl>…</note>
```

## Was im XML ausgezeichnet wird

Mit dem Verweis auf die Datenbank (`kbga-bibls-id`) bleibt die Auszeichnung im
XML minimal:

- die Lit-ID: `<bibl corresp="kbga-bibls-NNNN">`
- die Autor-ID: `<persName ref="kbga-actors-NNNN">`, bei Autoren, die ins gedruckte Register gehen
- Kursivierungen der Darstellung: `<hi rend="i">` für kursiv darzustellende Titel, `<hi rend="sup">` für hochgestellte Auflagezahlen

Zwischen Erscheinungsjahr und Auflagezahl steht kein Leerzeichen:
`1849<hi rend="sup">3</hi>`.

Alle weiteren bibliografischen Angaben werden in der Datenbank erfasst, nicht
im XML.

Querverweise auf andere Fussnoten, die nur der Auflösung zitierter Literatur
dienen, werden nicht eigens ausgezeichnet. Innerhalb von `<bibl>` erscheinen
keine Pop-ups (Ausnahme: `<ref>` auf andere Stellen in der Gesamtausgabe).

## Autor in `<bibl>`

Der Autor wird mit `<persName>` ausgezeichnet und in die Datenbank aufgenommen,
wenn die Person im Sinnhorizont des Haupttextes steht — wenn also der Autor
des Haupttextes den Namen gekannt und vermutlich im Sinn gehabt haben kann.
Bei Sekundärliteratur der Editoren erfolgt keine `persName`-Auszeichnung und
kein Datenbank-Eintrag. Siehe auch [Textelemente → Akteure](akteure.md).

"ders." wird nicht mit `<persName>` ausgezeichnet; der Autor erscheint im
Pop-up.

Beispiel für Sekundärliteratur (veröffentlicht 1989, Haupttext von 1934 — für
Barth nicht verfügbar):

```xml
<bibl corresp="kbga-bibls-1206">
  B. Jaspert, <hi rend="i">Der Kirchenhistoriker Heinrich Hermelink</hi>, 
  in: ders., <hi rend="i">Theologie und Geschichte. Gesammelte Aufsätze</hi>, 
  Bd. I, Frankfurt a. M. 1989, S. 219–239.
</bibl>
```

## Sonderfälle

### Barths eigene Literaturangaben

In Originaltexten und Originalfussnoten stellt Barth Literaturangaben
abweichend dar: der Autor wird kursiv, der Titel nicht kursiv dargestellt.

```xml
<note xml:id="ni" type="original">
  «<foreign xml:lang="lat">Non quod a se ipso…</foreign>» 
  (<bibl corresp="kbga-bibls-16">
    <persName ref="kbga-actors-77"><hi rend="i">Calvin</hi></persName>, 
    Inst. III 11, 9
  </bibl>).
</note>
```

### In kursivem Kontext

Innerhalb eines kursiv dargestellten Abschnitts (z.B. Vorworte,
`<div type="abstract">`) wird der Titel mit `<hi rend="text-recte">`
ausgezeichnet, damit er sich typographisch abhebt.

### Zeitungs- und Zeitschriftenartikel

Der Titel des Aufsatzes wird kursiv dargestellt, der Zeitschriftenname nicht:

```xml
<bibl corresp="kbga-bibls-1885">
  <persName ref="kbga-actors-636">[A.] K[elle]r</persName>, 
  <hi rend="i">Der Reformierte Weltbund in Zürich</hi>, 
  in: Neue Zürcher Zeitung vom 3.8.1923
</bibl>
```

Zeitschriftenartikel, deren Titel nicht genannt ist, werden nur unter dem
Namen der Zeitschrift erfasst.

### Lieder

Bibliografische Angaben zu Kirchenliedern werden nicht mit dem generischen
`<bibl>` ausgezeichnet, sondern mit `<bibl type="song">`. Siehe
[Textelemente → Lieder](lieder.md).

### Filme

Filme werden wie Literaturangaben behandelt:

```xml
den Film <bibl corresp="kbga-bibls-3244">«Hearts in Exile», 
der 1929 herauskam und auf deutsch den Titel «Verbannte Herzen»</bibl>
```

### Verweise auf KBGA-Bände

Für Verweise auf andere Bände der Karl-Barth-Gesamtausgabe wird
`<ref type="pub">` verwendet, wenn der Band online verfügbar ist. Für noch
nicht publizierte Bände wird `<ref type="pub-">` (mit Bindestrich):

```xml
<ref type="pub-" target="../texts?facet-volume=22">Vorträgen und kleineren Arbeiten 1909-1914</ref>
```
