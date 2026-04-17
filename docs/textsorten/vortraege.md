# Vorträge und kleinere Arbeiten (`<div type="paper">`)

Vorträge und kleinere Arbeiten werden mit `<div type="paper">` ausgezeichnet.
Jedes `<div>` innerhalb der Datei erzeugt online eine neue Seite.

## Grundstruktur

```xml
<div type="paper">
  <pb xml:id="p041" ed="pga"/>
  <head>GOTT ERKENNEN, GOTT EHREN, GOTT VERTRAUEN
    <lb/>NACH CALVINS KATECHISMUS</head>
  <head type="sub">1935</head>
  <div type="abstract">
    <p>…</p>
  </div>
  <div>
    <p>…</p>
  </div>
</div>
```

## Einleitung (`<div type="abstract">`)

Einleitungen des Herausgebers werden kursiv dargestellt (über das ODD).

### Einleitung mit mehreren Unterabschnitten

Um zu vermeiden, dass Unterabschnitte eigene Online-Seiten erzeugen,
werden die `<div>`-Elemente dem `<div type="abstract">` untergeordnet:

```xml
<div type="abstract">
  <div>
    <p>…</p>
  </div>
  <div>
    <head>…</head>
    <p>…</p>
  </div>
</div>
```

### Exkurs in der Einleitung

Ein `<div type="excursus">` innerhalb einer kursiven Einleitung wird
nicht kursiv dargestellt. Dazu wird jeder Absatz im Exkurs mit
`<p rend="text-recte">` markiert (siehe
[Textelemente → Hervorhebungen](../textelemente/hervorhebungen.md)
und [Textstruktur → Gliederung](../textstruktur/gliederung.md)).
