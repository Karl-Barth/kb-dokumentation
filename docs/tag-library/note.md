# `<note/>` (Anmerkung)

**Modul:** Kernmodule

## Beschreibung

enthält eine Anmerkung oder Annotation.

## Erläuterung

Ausführliche Dokumentation:

- [Textstruktur > Anmerkungen](https://dokumentation.karl-barth.ch/textstruktur/anmerkungen/)

## Erlaubt in

**Handschriftenbeschreibung:** [`<altIdentifier>`](altIdentifier.md)

## Inhaltsmodell

- *macro.specialPara*

## Beispiele

**Beispiel 1:**

```xml
And yet it is not only
        in the great line of Italian renaissance art, but even in the
        painterly
<note place="bottom" type="gloss" resp="#MDMH-1"><term xml:lang="de">Malerisch</term>. This word has, in the German, two
          distinct meanings, one objective, a quality residing in the object,
          the other subjective, a mode of apprehension and creation.  To avoid
          confusion, they have been distinguished in English as
          <mentioned>picturesque</mentioned> and
          <mentioned>painterly</mentioned> respectively.</note> style of the
        Dutch genre painters of the seventeenth century that drapery has this
        psychological significance.
<!-- elsewhere in the document -->
<respStmt xml:id="MDMH-1">
         <resp>translation from German to English</resp>
         <name>Hottinger, Marie Donald Mackie</name>
       </respStmt>
```

**Beispiel 2:**

```xml
Mevorakh b. Saadya's mother, the matriarch of the
      family during the second half of the eleventh century,
<note n="126" anchored="true"> The
        alleged mention of Judah Nagid's mother in a letter from 1071 is, in fact, a reference to
        Judah's children; cf. above, nn. 111 and 54. </note> is well known from Geniza documents
      published by Jacob Mann.
```
