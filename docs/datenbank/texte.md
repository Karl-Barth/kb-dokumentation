# Texte

## Vorlagen

Vorlagen der Edition werden in der Datenbank mit den Texte verknüpft. Die Vorlagen werden beim Export der Daten in den TeiHeader in die `<sourceDesc>` geschrieben und können dann in dien [textkritischen Fussnoten](../textstruktur/anmerkungen.md#verweis-auf-vorlagen) referenziert werden.

Bei Drucken wird die Vorlage zuerst in der Literaturdatenbank erfasst. Und anschliessend mit dem Text verknüpft. Ansonsten werden die Vorlagen aus dem Karl Barth-Archiv verknüpft.

Die Beziehung zwischen Vorlage und Text wird immer mit einem Grossbuchstaben "A", "B", "C" benannt, egal ob es sich um einen Druck oder eine Handschrift handelt. Als "A" wird immer die Hauptvorlage bezeichnet, die direkt für die Edition verwendet wurde.

Verschiedene Beziehungen zum edierten Text (offene Liste) sind möglich:

* Vorlage der Edition
* Weitere Vorlage
* Weiteres Material 
* Weiterer Druck
* Weiteres Manuskript
* Material zum Kontext \[nur wenn sehr wichtig\]
* Exemplar von A
* Grundlage von A [Typoskript/Manuskript von A]
* Vorarbeit zu A [z.B. Stichwortkonzept]

Wenn im KBA ein Exemplar einer Druckvorlage existiert, dann werden die bibliografischen Angaben aus den bibls mit A "Vorlage der Edition" und der KBA Eintrag mit A1 "Exemplar von A" verknüpft.

## Titel im teiHeader

Die Titel in der `<titleStmt>` werden beim Export aus der Datenbank erzeugt, nicht im XML gepflegt.

```xml
<titleStmt>
  <title type="volume" n="vol-02">Ethik I</title>
  <title type="section" n="II">Akademische Werke</title>
  <title type="content">Ethik und Dogmatik</title>
  …
</titleStmt>
```

| `@type` | Inhalt | Quelle in der Datenbank |
|---|---|---|
| `volume` | Bandtitel, `@n` = Band (`vol-02`) | Band: Titel |
| `section` | Abteilung der Gesamtausgabe, `@n` = römische Abteilungsnummer | Band: Abteilung |
| `formal` | Formaler Titel im Band, z.B. «Vorwort», «Brief Nr. 4» | Text: formaler Titel |
| `content` | Inhaltlicher Titel, z.B. «Karl Barth an Rudolf Bultmann» | Text: inhaltlicher Titel |
| `citation_line_1` bis `_3` | Zitiervorschlag: Titel mit Datum, URL mit Stand, Angabe des Drucks | erzeugt |

Die Abteilungen der Gesamtausgabe:

| `@n` | Abteilung |
|---|---|
| I | Predigten |
| II | Akademische Werke |
| III | Vorträge und kleinere Arbeiten |
| IV | Gespräche |
| V | Briefe |
