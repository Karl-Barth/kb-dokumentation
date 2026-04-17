# Vorlesungsreihen (`<div type="chapter">`)

Vorlesungsreihen werden mit `<div type="chapter">` gegliedert; die
einzelnen Vorlesungseinheiten mit `<div type="session">`. Pro `<div>`
wird online eine eigene Seite dargestellt.

Die Dateien sind nach Hauptkapiteln geordnet, die durch die Tage der
jeweiligen Vorlesungen untergliedert sind.

## Kapitel und Vorlesungseinheit

### Neues Kapitel am Vorlesungsbeginn

Folgt `<div type="session">` direkt auf `<div type="chapter">` ohne
einen `<p>` dazwischen, wird **keine** neue Online-Seite erzeugt:

```xml
<body>
  <div type="chapter">
    <pb ed="pga" xml:id="p003"/>
    <head>DIE THEOLOGIE ZWINGLIS</head>
    <div type="session">
      <head>§ 1 ZWINGLI IM URTEIL DES LUTHERTUMS</head>
      <p><date rend="right">2.XI.22</date> …</p>
    </div>
  </div>
</body>
```

### Fortsetzung an einem anderen Vorlesungstag

Ein weiteres `<div type="session">` innerhalb desselben Kapitels erzeugt
eine neue Online-Seite:

```xml
<div type="session">
  <p><date rend="right">6.XI.22</date> Ähnlich steht es bei …</p>
</div>
```

Das Datum der Vorlesung wird mit `<date rend="right">` ausgezeichnet und
erscheint am rechten Seitenrand.

### Hauptüberschrift hat Vorrang

Die Dateien sind nach Hauptkapiteln gegliedert; diese bestimmen den
Seitenumbruch. Beginnt innerhalb eines Vorlesungstags ein neues Kapitel,
wird das Datum **nicht** wiederholt.

Siehe auch [Textstruktur → Gliederung](../textstruktur/gliederung.md).
