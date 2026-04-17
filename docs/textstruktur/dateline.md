# Datum mit Ortsangabe (`<dateline>`)

```xml
<dateline>
  <placeName ref="kbga-places-54">Safenwil</placeName>, Sonntag, den 
  <date when="1912-09-08">8. September 1912</date>
</dateline>
```

`<dateline>` fasst eine Datums- und Ortsangabe zusammen, die einem Text
voran- oder nachgestellt ist. Das Element steht innerhalb von `<opener>`
(Briefkopf, Predigtkopf) oder `<closer>` (Unterschrift).

## In Predigten

Standardmässig wird die `<dateline>` über das ODD linksbündig dargestellt,
mit der Seitenzahl am rechten Rand in derselben Zeile.

Wurde eine Predigt an mehreren Orten gehalten, werden die Angaben mit
`<lb/>` getrennt:

```xml
<dateline>
  <placeName ref="kbga-places-426">Seon</placeName>, Mittwoch, den 
  <date when="1915-02-17">17. Februar 1915</date>
  <lb/>
  <placeName ref="kbga-places-54">Safenwil</placeName>, Sonntag, den 
  <date when="1915-02-21">21. Februar</date> (Friedensbettag)
</dateline>
```

## In Briefen

Ohne weitere Attribute wird die `<dateline>` rechtsbündig dargestellt;
die Anrede (`<salute>`) erscheint linksbündig in derselben Zeile:

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

### Absenderangabe

Enthält der Briefkopf eine Absenderangabe, wird diese in einer eigenen
`<dateline rend="sender">` erfasst:

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

## In Unterschriften

In Vorworten und ähnlichen Texten kann `<dateline>` auch in `<closer>`
stehen:

```xml
<closer>
  <dateline rend="left">Schiers (Graubünden), am 26. Oktober 1989</dateline>
  <signed rend="right">Holger Finze</signed>
</closer>
```

Siehe auch [Textstruktur → Unterschriften](unterschriften.md).

Genre-spezifische Beispiele: [Textsorten → Predigten](../textsorten/predigten.md),
[Textsorten → Briefe](../textsorten/briefe.md).

## Abweichende Ausrichtung

Muss die Ausrichtung vom Standard abweichen (z.B. eine Adresse auf der
rechten Seite), wird `@rendition="right"` bzw. `@rendition="left"` verwendet:

```xml
<dateline rendition="right">
  <placeName ref="kbga-places-10">Bonn</placeName>, den 
  <date when="1931-01-28">28.1.1931</date>
</dateline>
<address rendition="left">
  <addrLine>Tageb. 68</addrLine>
</address>
```
