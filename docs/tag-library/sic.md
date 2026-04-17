# `<sic>` Lateinisch für 'auf diese Weise', 'so'

Markiert die fehlerhafte Stelle in der Druckausgabe (innerhalb von choice/sic/corr). Das @ed gibt die Ausgabe an (typisch: pga).

Siehe [Textelemente > Korrektionen Der Druckausgabe](https://dokumentation.karl-barth.ch/textelemente/korrektionen-der-druckausgabe/)

**Modul:** core — Kernmodule

## Attribute

**att.edition** provides attributes identifying the source edition from which some encoded feature derives.

**@ed** (optional)
:   Datentyp: teidata.word

**@edRef** (optional)
:   Datentyp: teidata.pointer


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


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


## Beispiele

**Beispiel 1:**

```xml
I don't know, Juan. It's so far in the past now
      — how
<sic>we can</sic> prove or disprove anyone's theories?
```

**Beispiel 2:**

```xml
I don't know, Juan. It's so far in the past now
      — how
<choice>
  <sic>we can</sic>
  <corr>can we</corr>
</choice> prove or disprove anyone's theories?
```

## Content Model

```xml
<content>
  <macroRef key="macro.paraContent"/>
</content>
```
