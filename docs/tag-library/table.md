# `<table>` Tabelle

enthält Text, der in Tabellenform, also in Zeilen und Spalten, dargestellt ist.

Enthält eine Reihe von Zeilen und optional eine Überschrift.
    Jegliche Information die grafische Darstellung betreffend, sollte mit dem globalen
      rend-Attribut auf der Ebene von Tabelle, Zeile oder Zelle verzeichnet werden.

Siehe [Textstruktur > Tabellen](https://dokumentation.karl-barth.ch/textstruktur/tabellen/)

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


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


**@rows** (optional)
:   gibt die Anzahl der Tabellenzeilen an.
:   Datentyp: teidata.count

**@cols** (optional)
:   gibt die Anzahl der Tabellenspalten an.
:   Datentyp: teidata.count


## Kann enthalten

**figures:** [row](row.md) "enthält eine Zeile einer Tabelle."

## Content Model

```xml
<content>
    <sequence>
      
        <alternate minOccurs="0" maxOccurs="unbounded">
          <classRef key="model.headLike"/>
          <classRef key="model.global"/>
        </alternate>
      
      <alternate>
        <sequence minOccurs="1" maxOccurs="unbounded">
          <elementRef key="row"/>
          
            <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
          
        </sequence>
        <sequence minOccurs="1" maxOccurs="unbounded">
          
            <classRef key="model.graphicLike"/>
          
          
            <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
          
        </sequence>
      </alternate>
      <sequence minOccurs="0" maxOccurs="unbounded">
        
          <classRef key="model.divBottom"/>
        
        
          <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
        
      </sequence>
    </sequence>
  </content>
```
