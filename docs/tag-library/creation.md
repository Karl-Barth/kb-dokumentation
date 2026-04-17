# `<creation>` Entstehung

beinhaltet Informationen zur Entstehung eines Textes.

Das creation-Element kann dafür verwendet werden, Einzelheiten über die Entstehung eines Textes, 
          z. B. Entstehungszeit und Entstehungsort, zu dokumentieren, wenn diese von Interesse sind. 
          Es kann auch eine mehr oder weniger strukturierte Entstehungsgeschichte mit den einzelnen Bearbeitungs- und Revisionstufen 
          enthalten; diese sollten mithilfe des listChange-Elements ausgezeichnet werden. Das creation-Element darf 
          aber nicht mit dem publicationStmt-Element, das Zeit und Ort der Veröffentlichung verzeichnet, verwechselt werden.

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


## Kann enthalten

Beliebiger Textinhalt

## Content Model

```xml
<content>
    <alternate minOccurs="0" maxOccurs="unbounded">
      <textNode/>
      <classRef key="model.limitedPhrase"/>
      <elementRef key="listChange"/>
    </alternate>
  </content>
```
