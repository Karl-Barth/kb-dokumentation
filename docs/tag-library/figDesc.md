# `<figDesc>` Beschreibung einer Abbildung

enthält einen kurzen Beschreibungstext des Inhalts oder des Aussehens einer Abbildung, um etwa
    ein Bild ohne dessen Anzeige dokumentieren zu können.

Dieses Element ist als Ersatz für den Inhalt seines Elternelements figure gedacht. Zum
      Beispiel wenn das Bild nicht angezeigt werden kann und man auf einen Alternativtext angewiesen
      ist. Es kann weiters für Indexierungen und Dokumentationen benutzt werden.

Siehe [Textstruktur > Bilder](https://dokumentation.karl-barth.ch/textstruktur/bilder/)

**Modul:** figures — Abbildungen und Tabellen

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


## Enthalten in

**figures:** [figure](figure.md) "Abbildung mit optionaler Beschreibung (figDesc) und Grafik ("

## Content Model

```xml
<content>
    <macroRef key="macro.limitedContent"/>
  </content>
```
