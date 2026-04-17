# `<author>` Autor

Verfasserangabe im teiHeader. Das @ref verweist auf die Personen-ID in der Meta-DB.

Insbesondere wenn eine Katalogisierung auf Basis des TEI-Headers erfolgen soll, ist es ratsam
      einen Namen aus einer annerkannten Normdatei zu verwenden. Die Attribute key und
      ref können außerdem benutzt werden, um auf kanonische Informationen über
      einen Autor zu verweisen, etwa in einem Bibliothekskatalog oder einer Online-Ressource.
    Im Fall von Rundfunksendungen sollte dies Element benutzt werden, um den Namen der Firma oder
      der Sendergruppe zu notieren, welche diese Rundfunksendung verantwortet.
    Wo ein Autor unbekannt oder nicht angegeben ist, kann dieses Element Text wie z. B.
      Unbekannt oder Nicht angegeben beinhalten.
      Wenn die entsprechenden TEI-Module benutzt werden, kann das Element auch detaillierte
      Auszeichnungen für Namen von Personen, Organisationen oder Orten beinhalten - insbesondere
      wenn mehrere Namen vorhanden sind.

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


**att.datable** provides attributes for normalization of elements
    that contain dates, times, or datable events.

**@period** (optional)
:   Datentyp: teidata.pointer


**att.naming** provides attributes common to elements which refer to named persons, places, organizations etc.

**@role** (optional)
:   Datentyp: teidata.enumerated


**@ref** (optional)
:   Datentyp: teidata.pattern


## Content Model

```xml
<content>
  <macroRef key="macro.phraseSeq"/>
</content>
```
