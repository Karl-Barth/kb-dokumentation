# Briefe (`<div type="letter">`)

```xml
<div type="letter">
  <pb xml:id="p003" ed="pga"/>
  <head>1</head>
  <opener>
    <dateline>…</dateline>
    <salute>…</salute>
  </opener>
  <p>…</p>
  <closer>
    <salute>…</salute>
    <signed>…</signed>
  </closer>
</div>
```

Briefe werden online auf einer Seite dargestellt. Die Briefnummer steht
in `<head>`. Zwischen `<opener>` und `<closer>` erfolgen keine weiteren
gesondert ausgezeichneten Texteinheiten.

## Briefkopf (`<opener>`)

### Ohne Absenderangabe

```xml
<opener>
  Bultmann
  <dateline>
    <placeName ref="kbga-places-41">Marburg</placeName>,
    <date when="1922-05-25">25.V.1922</date>
  </dateline>
  <salute>Lieber Herr <persName ref="kbga-actors-2151">Barth</persName>!</salute>
</opener>
```

Die `<dateline>` wird rechtsbündig dargestellt, die Anrede linksbündig
in derselben Zeile. Siehe auch
[Textstruktur → Datum mit Ortsangabe](../textstruktur/dateline.md).

### Mit Absenderangabe

Die Absenderzeile wird in einer eigenen `<dateline rend="sender">` erfasst:

```xml
<opener>
  <dateline rend="sender">
    <persName ref="kbga-actors-223">von Kirschbaum</persName> an
    <persName ref="kbga-actors-2151">B.</persName> in
    <placeName ref="kbga-places-44">Münster</placeName>
  </dateline>
  <dateline>
    [<placeName ref="kbga-places-757">Krefeld</placeName>]
    <date when="1926-02-27">27.2.1926</date>
  </dateline>
  <salute>Lieber <persName ref="kbga-actors-2151">Karl</persName>,</salute>
</opener>
```

### Mit Anschrift

```xml
<opener>
  <dateline rendition="right">
    <placeName ref="kbga-places-44">Münster</placeName>, den
    <date when="1929-11-28">28. November 1929</date>
  </dateline>
  <address rendition="left">
    <addrLine>An den</addrLine>
    <addrLine>Herrn Minister</addrLine>
    <addrLine><orgName ref="kbga-actors-8245">für Wissenschaft, Kunst und
      Volksbildung</orgName></addrLine>
    <addrLine><hi rend="i"><placeName ref="kbga-places-8">Berlin</placeName></hi></addrLine>
  </address>
</opener>
```

## Grussformel (`<closer>`)

Siehe [Textstruktur → Unterschriften](../textstruktur/unterschriften.md).

```xml
<closer>
  <salute>Mit herzlichem Gruß!</salute>
  <signed><persName ref="kbga-actors-2151">Karl Barth</persName></signed>
</closer>
```

Bei mehrzeiligen Grussformeln wird über das ODD das erste Grußwort
linksbündig, die weiteren rechtsbündig dargestellt.

## Nachschrift (`<postscript>`)

Dem Grußwort nachgestellte Texte:

```xml
<postscript>
  <p>In der nächsten Nr.…</p>
</postscript>
```
