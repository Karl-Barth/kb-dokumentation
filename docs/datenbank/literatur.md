# Literatur

`bibls` werden wie `actors` oder `places` als Entitäten in der Meta-Datenbank erfasst. Dieses Vorgehen ersetzt die detaillierte Auszeichnung von `<bibl>` im TEI. Dort müssen nur noch Kursivierungen gekennzeichnet werden.

Grundsätzlich wird versucht, die Entität `bibl` kompatibel zu [biblatex](https://mirror.init7.net/ctan/info/translations/biblatex/de/biblatex-de-Benutzerhandbuch.pdf) und zur TEI (`bibl`) umzusetzen. Eintragstypen und Eingabefelder entsprechen jeweils biblatex-Vorgaben.

Wenn Einträge mit den bestehenden Feldern und Typen nicht adäquat erstellt werden können, kann im Feld xml_raw die Angabe in XML direkt codiert werden.

!!! note ""
    Es soll versucht werden die Gesamtbibliografie konsistent zu halten. Kleinere Abweichungen in der Darstellung (o.ä.) zu konkreten Angaben in der gedruckten Ausgabe spielen normalerweise keine Rolle.

## Klassiker
Für Klassiker, die ohne bibliografische Angaben zitiert werden, wird eine Referenzausgabe in der Datenbank aufgenommen. Beispiele: Confessio Augustana, Goethes Faust usw.

## Typen
Für das angezeigte Formular wie für die Formatierung des Eintrags, ist der Eintragstyp (Bibl Typ) entscheiden. Dieser ist deshalb zwingend auszufüllen. Die bereitstehenden Typen können bei Bedarf um weitere Typen erweitert werden.

| Bezeichnung in der DB | biblatex | Kommentar |
|-----------------------|----------|-----------|
| Monografie | book | Bücher, auch mehrbändige Werke |
| Buchteil | inbook | Kapitel, Aufsätze in einem Buch, bei dem der Verfasser identisch ist |
| Zeitschriftenartikel | article | auch Zeitungsartikel |
| Sammelband-Beitrag | incollection | Aufsätze in Bänden, die von anderen herausgegeben wurden |
| Sammelband | collection | mit mehreren unabhängigen Beiträgen (Aufsätze, Lexikonartikel, u.U. auch Quelleneditionen) |
| Reihe | periodical | Zeitschriften und Reihen; auch abgekürzt möglich |
| Lexikonartikel | reference |  |
| Doktorarbeit | thesis | wie Monografie, für die Angabe des Types (z.B. «Diss.») wird `edition` verwendet [Beispiel](https://meta.karl-barth.ch/bibls/349) |
| Anderes | generic | sollte keinesfalls verwendet werden |
| Website | online | Originaltexte im Internet [Beispiel](https://meta.karl-barth.ch/bibls/763) |
| xml-raw | \- | für Einträge verwenden, die zu komplexe für die DB sind |

## Autor(inn)en, Editor(inn)en und Orte

Autoren, Editoren und Orte können, müssen aber keine `kbga-actor-id` enthalten.

Bei Eingabe der `id` wird automatisch eine Verknüpfung zu den Akteuren/Orten gemacht.

## Titel

### Buchtitel (insb. bei mehrbändigen Werke)

Im Buchtitel kann mit `::` eine Segmentierung verschiedener Titelteile vorgenommen werden. Dabei können 3 Fälle unterschieden werden:

1) `Buchtitel :: Titelzusatz`  
2) `Hauptitel :: Bandangabe :: Buchtitel`  
3) `Hauptitel :: Bandangabe :: Buchtitel :: Titelzusatz`

Die zusätzlichen "Felder" entsprechen den Feldern `maintitle` und `titleaddon` in `biblatex`.

### Aufsatztitel

Bei Aufsatztiteln kann ebenfalls ein Titelzusatz angegeben werden:

- `Aufsatztitel :: Titelzusatz`

Standardmässig wird dieser in der Anzeige dann mit Komma abgetrennt. Handelt es sich um eine Jahresangabe (Originalerscheinungsjahr des Aufsatzes), wird dieses in Klammern gesetzt [`kbga-bibl-479`](https://meta.karl-barth.ch/bibls/479):

```plaintext
Das Evangelium in der Gegenwart :: [1935]
```

In Zeitschriften und insb. in Zeitungen wird manchmal kein Titel angegeben. Wenn es kein Titel gibt, wird nur die Zeitschrift als Ganzes getaggt.

### Titel von Zeitschriften und Reihen

Die Titel von Zeitschriften und Reihen werden häufig abgekürzt. In bibls kann sowohl die Abkürzung als auch bevorzugt die ausgeschriebene Variante verwendet werden. Wenn die abgekürzte Variante verwendet wird, muss diese über die Abkürzungen in der DB auflösbar sein, und zwar so, dass die Auflösung ausschliesslich den Titel der Zeitschrift oder Reihe enthält.

### Zeitschriftenartikel ohne Autor und ohne Titel

Werden Zeitschriftenartikel ohne Autor und ohne Titel zitiert, wird die Zeitschrift als Reihe in der DB getaggt.




<!-- TEI title @level
Die Angabe der Titel richtet sich grundsätzlich nach den `@level` wie sie in der TEI definiert sind.
| Bezeichnung in der DB | level | Kommentar |
|-----------------------|-------|-----------|
| Aufsatztitel | a | unselbständiger Titel |
| Buchtitel | m |  |
| Zeitschrift | j | auch abgekürzt verwendbar, wenn eine Auflösung in den Abkürzungen gefunden werden kann |
| Reihe | s | auch abgekürzt verwendbar, wenn eine Auflösung in den Abkürzungen gefunden werden kann |
| unpublizierter Titel | u | noch nicht realisiert |
-->


## Auflage, Ausgabe
Um die Auflage anzugeben, kann im Feld Auflgabe (edition) eine Zahl angegeben werden. Wenn mehr zur Ausgabe bekannt ist, kann hier auch der volle Text dazu eingegeben werden (z.B. "3. vollständig überarbeitete Ausgabe"). Ist beispielsweise das Jahr der Auflage bekannt kann es wie folgt angegeben werden: 3. Auflage 1988

Werden verschiedene Auflagen zitiert, ist festzustellen ob diese voneinander abweichen. Wenn zwei Ausgaben z.B. unterschiedlich umangreich sind, müssen beide Ausgaben aufgenommen werden. Bei unveränderten Nachdrucken oder Neuauflagen genügt ein Eintrag in der Datenbank.

Im Zweifelsfall (Auflagenvergleich u.ä.) in der DNB nachschlagen:

- [https://portal.dnb.de](https://portal.dnb.de)
- [https://kvk.bibliothek.kit.edu/?digitalOnly=0&embedFulltitle=0&newTab=0](https://kvk.bibliothek.kit.edu/?digitalOnly=0&embedFulltitle=0&newTab=0)

## Abkürzungen
Werden insbesondere dann verwendet, wenn eine Reihe oder eine Zeitschrift als Ganzes erfasst wird.

## URL
Es kann ein Link auf den Text/die Ausgabe im Internet und ein Datum, wann diese zuletzt gecheckt wurde, eingegeben werden. Bei originalen Webpublikationen ist der Typ "Website" auszuwählen.

## Filme
<!-- Bei Filmen wird die ganze Angabe in der Fussnote getaggt.-->

In der DB werden folgende Felder ausgefüllt: 

- bibl-Typ = Film
- Autor:innen = Regisseur:in
- Buchtitel = Filmtitel
- Publikationsdatum

Als Resource wird der Wikipedia-Eintrag zum Film. Falls dieser nicht verfügbar ist, wird der englische Wikipedia-Eintrag (provider: wikipedia en) manuell verlinkt. Der Eintrag auf die IMDb ist ebenfalls manuell zu verlinken (z.B. Provider = IMDb, Provider-ID (letzter Teil der URL) = tt0021572, URL = [https://www.imdb.com/title/tt0021572/](https://www.imdb.com/title/tt0021572/))
