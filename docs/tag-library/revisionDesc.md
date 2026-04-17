# `<revisionDesc>` Beschreibung der Dateihistorie

dokumentiert die Änderungen, die an der Datei vorgenommen wurden.

Wenn an diesem Element gesetzt, sollte das status-Attribut den aktuellen 
          Status des Dokuments widerspiegeln. An jedem change-Kindelement gibt das selbe 
          Attribut den jeweiligen Status zum Zeitpunkt der Änderung an. Die change-Elemente 
          werden der Konvention nach so angeordnet, dass die letzte Änderung am Anfang steht und die erste zum Schluss.

[TEI Guidelines: revisionDesc](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-revisionDesc.html)

**Modul:** header — Header

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
