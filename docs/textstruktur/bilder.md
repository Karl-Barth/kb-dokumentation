# Bilder (`<figure>`)

```xml
<figure rendition="simple:display">
  <graphic url="../images/53/Abb-1.jpg"/>
  <figDesc><hi rend="i">Abb. 1: Rosenlaui mit Wellhorn (3196m) 
    und Wetterhorn (3703m)</hi></figDesc>
</figure>
```

Bilder werden mit `<figure>` und `<graphic>` eingebaut. Die URL wird als
relativer Pfad zum Bilderverzeichnis des Bandes angegeben:
`../images/Bd.-Nummer/Bildname`.

In `<figDesc>` wird die Bildunterschrift eingetragen.

## Positionierung

### Bild am Seitenanfang

Der Absatz vor dem Bild muss geschlossen werden (`</p>`), nach dem Bild
wird ein neuer Absatz geöffnet. Falls das Bild auf einer neuen Seite
beginnt, wird `<pb>` im `<head>` des `<figure>` eingetragen:

```xml
</p>
<figure rendition="simple:display">
  <head><pb rend="noPipe" xml:id="p011" ed="pga"/></head>
  <graphic url="../images/53/Abb-1.jpg"/>
  <figDesc>…</figDesc>
</figure>
<p>…
```

### Bild innerhalb einer Fussnote

Mit `<figure rend="inline">` wird das Bild mittig zum umgebenden Text
dargestellt:

```xml
<note xml:id="n35">Folgende Zeichnung findet sich am Mskr.-Rand:
  <figure rend="inline">
    <graphic url="../images/40/Abb-1.png"/>
  </figure>
</note>
```

## Bilddateien

Die Bilddateien werden in `kb_xml_src` im Verzeichnis
`vol-NN/images/` des entsprechenden Bandes abgelegt.
