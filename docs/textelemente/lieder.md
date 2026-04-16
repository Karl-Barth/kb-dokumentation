# Lieder (`<bibl type="song">`)

```xml
<bibl type="song" corresp="kbga-songs-57">Nr. 43: «Morgenglanz der Ewigkeit» von 
<persName ref="kbga-actors-2060">Chr. Knorr von Rosenroth</persName>, Strophen 1-3 
(= GERS [1952] 80,1-3; EG 450,1-3)</bibl>
```

Bibliographische Referenzen auf Kirchenlieder werden mit `<bibl type="song">`
ausgezeichnet. Das Attribut `@corresp="kbga-songs-NNNN"` verweist auf den
Eintrag in der Lieder-Datenbank.

Datenbank-spezifisches (Gesangbuch-Abkürzungen, Verwendung in den einzelnen
Bänden) siehe [Datenbank → Lieder](../datenbank/lieder.md). Für den wörtlichen
Liedtext im Fliesstext siehe [Textstruktur → Gedichte](../textstruktur/gedichte.md).

## Was wird ausgezeichnet

Kirchenlieder aus gängigen Gesangbüchern werden in der Lieder-Datenbank
verzeichnet und mit `<bibl type="song" corresp="kbga-songs-…">` ausgezeichnet.
Lieder für regionale Gesangbücher werden ohne Liednummer erfasst.

Andere Lieder (nicht in Gesangbüchern) werden als regulärer Literatureintrag
erfasst und mit `<bibl corresp="kbga-bibls-…">` ausgezeichnet.

Ausgezeichnet werden nur:

- die Lied-ID (Attribut `@corresp`, aus der Lieder-Datenbank)
- die Autor-ID (Attribut `@ref` in `<persName>`, aus dem Akteure-Register)

Der Liedtitel wird nicht kursiv dargestellt und nicht gesondert ausgezeichnet;
alle weiteren Angaben erscheinen im Pop-up.

## Strophenangaben

Zwischen Liednummer und Strophenangabe steht kein Leerzeichen; das Komma
trennt direkt:

- `GERS [1952] 292,1-2`
- `Strophen 1,2,4`
- `(= EKG 197, Str. 1–4,8)`
- `Strophen 1-3.7.10.11`

Bei Trennung mehrerer Strophenbereiche durch Semikolon folgt auf das Semikolon
ein Leerzeichen:

- `Strophen 1–3; 4–6`

## Liedliste am Ende einer Predigt

Barth hat in einigen Bänden die in der Predigt gesungenen Lieder im
Predigtkopf vermerkt (seit dem 1. November 1914 regelmässig). In Band 5 stehen
sie in der ersten Fussnote, in anderen Bänden als Liste am Ende der Predigt.

## Lieder innerhalb einer Fussnote

Sind die Lieder in der gedruckten Edition in einer Fussnote angegeben, werden
sie auch digital in der Fussnote wiedergegeben und nicht in eine Liedliste
überführt — meist ist dann eine gedruckte Predigt die direkte Vorlage, und
die Lieder wurden aus dem Manuskript ergänzt.
