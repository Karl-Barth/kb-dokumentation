# `<note>` Anmerkung

Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @type unterscheidet Fussnoten und editorische Anmerkungen.

Siehe [Textstruktur > Anmerkungen](https://dokumentation.karl-barth.ch/textstruktur/anmerkungen/)

**Modul:** core — Kernmodule

## Attribute

**att.global** stellt gemeinsame Attribute für alle Elemente im TEI-Kodierungsschema bereit.

**@xml:id** (optional)
:   liefert einen Identifikator für das Element, welches dieses Attribut trägt.
:   Datentyp: ID

**@n** (optional)
:   gibt eine Nummer (oder eine andere Bezeichnung) für ein Element an, die innerhalb des Dokuments nicht zwangsläufig eindeutig ist.
:   Datentyp: teidata.text

**@xml:lang** (optional)
:   gibt die Sprache des Elementinhalts durch ein Tag an, das nach BCP 47 festgelegt wird.
:   Datentyp: teidata.language

**@xml:base** (optional)
:   liefert eine Basis-URI-Referenz, mit der Anwendungen relative URI-Referenzen in absolute auflösen können.
:   Datentyp: teidata.pointer

**@xml:space** (optional, geschlossene Werteliste)
:   signalisiert die gewünschte Handhabung von Leerzeichen durch Anwendungen.
:   Datentyp: teidata.enumerated
:   `default`
:   `preserve`


**att.anchoring** provides attributes for use on annotations, e.g. notes and groups of notes
  describing the existence and position of an anchor for annotations.

**@anchored** (optional)
:   gibt an, ob eine Vorlage den exakten Referenzort der Anmerkung anzeigt.
:   Datentyp: teidata.truthValue

**@targetEnd** (optional)
:   verweist auf das Ende eines Bereichs, dem das note-Element angefügt ist, es sei denn die
        Anmerkung ist in den Text an diesem Punkt bereits eingebettet.
:   Datentyp: teidata.pointer


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


**att.placement** provides attributes for describing where on the source page or
  object a textual element appears.

**@place** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `top`
:   `bottom`
:   `margin`
:   `opposite`
:   `overleaf`
:   `above`
:   `right`
:   `below`
:   `left`
:   `end`
:   `inline`
:   `inspace`


**att.pointing** provides a set of attributes used by all elements which point
  to other elements by means of one or more URI references.

**@target** (optional)
:   Datentyp: teidata.pointer


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


## Enthalten in

**msdescription:** [altIdentifier](altIdentifier.md) "Alternativer Identifikator für eine Quelle (URI, KBA-ID, KBG"

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

## Content Model

```xml
<content>
  <macroRef key="macro.specialPara"/>
</content>
```
