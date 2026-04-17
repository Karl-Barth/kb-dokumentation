# `<licence>`

beinhaltet für den Text gültige Lizenzinformationen oder andere rechtswirksame Vereinbarungen.

Das licence-Element soll für jede Lizenzvereinbarung, 
          die sich auf den Text bezieht, angegeben werden. Das target-Attribut 
          kann verwendet werden, um auf eine vollständige Version der Lizenz zu referenzieren. Die Attribute when, notBefore, notAfter, from oder to können in Kombination verwendet werden, um den Gültigkeitszeitraum der Lizenz anzugeben.

**Modul:** header — Header

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


**att.datable** provides attributes for normalization of elements
    that contain dates, times, or datable events.

**@period** (optional)
:   Datentyp: teidata.pointer


**att.pointing** provides a set of attributes used by all elements which point
  to other elements by means of one or more URI references.

**@target** (optional)
:   Datentyp: teidata.pointer


## Content Model

```xml
<content>
    <macroRef key="macro.specialPara"/>
  </content>
```
