# `<revisionDesc/>` (Beschreibung der Dateihistorie)

**Modul:** Header

## Beschreibung

dokumentiert die Änderungen, die an der Datei vorgenommen wurden.

## Erläuterung

Wenn an diesem Element gesetzt, sollte das status-Attribut den aktuellen 
          Status des Dokuments widerspiegeln. An jedem change-Kindelement gibt das selbe 
          Attribut den jeweiligen Status zum Zeitpunkt der Änderung an. Die change-Elemente 
          werden der Konvention nach so angeordnet, dass die letzte Änderung am Anfang steht und die erste zum Schluss.

## Erlaubt in

**Header:** [`<teiHeader>`](teiHeader.md)

## Inhaltsmodell

- [`<list>`](list.md)
- `<listChange>`
- [`<change>`](change.md)
