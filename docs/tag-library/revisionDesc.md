# `<revisionDesc>` Beschreibung der Dateihistorie

dokumentiert die Änderungen, die an der Datei vorgenommen wurden.

Wenn an diesem Element gesetzt, sollte das status-Attribut den aktuellen 
          Status des Dokuments widerspiegeln. An jedem change-Kindelement gibt das selbe 
          Attribut den jeweiligen Status zum Zeitpunkt der Änderung an. Die change-Elemente 
          werden der Konvention nach so angeordnet, dass die letzte Änderung am Anfang steht und die erste zum Schluss.

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


## Enthalten in

**header:** [teiHeader](teiHeader.md) "wird aus der Meta- und Registerdatenbank erzeugt und soll im"

## Kann enthalten

**core:** [list](list.md) "Liste. Der @type unterscheidet geordnete und ungeordnete Lis"

**header:** [change](change.md) "Änderungsvermerk in der revisionDesc. Enthält Zeitstempel de"

## Content Model

```xml
<content>
    <alternate>
      <elementRef key="list" minOccurs="1" maxOccurs="unbounded"/>
      <elementRef key="listChange" minOccurs="1" maxOccurs="unbounded"/>
      <elementRef key="change" minOccurs="1" maxOccurs="unbounded"/>
    </alternate>
  </content>
```
