# `<creation>` Entstehung

beinhaltet Informationen zur Entstehung eines Textes.

Das creation-Element kann dafür verwendet werden, Einzelheiten über die Entstehung eines Textes, 
          z. B. Entstehungszeit und Entstehungsort, zu dokumentieren, wenn diese von Interesse sind. 
          Es kann auch eine mehr oder weniger strukturierte Entstehungsgeschichte mit den einzelnen Bearbeitungs- und Revisionstufen 
          enthalten; diese sollten mithilfe des listChange-Elements ausgezeichnet werden. Das creation-Element darf 
          aber nicht mit dem publicationStmt-Element, das Zeit und Ort der Veröffentlichung verzeichnet, verwechselt werden.

[TEI Guidelines: creation](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-creation.html)

**Modul:** header — Header

## Enthalten in

**header:** [profileDesc](profileDesc.md) "enthält eine detaillierte Beschreibung der nicht-bibliografi"

## Kann enthalten

Beliebiger Textinhalt

**core:** [abbr](abbr.md) "Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref" [address](address.md) "enthält eine Postadresse, z. B. eines Verlegers, einer Organ" [choice](choice.md) "Gruppiert sic/corr-Paare für Korrekturen der Druckausgabe." [date](date.md) "Datumsangabe mit maschinenlesbarem Datum in @when, @from/@to" [foreign](foreign.md) "Fremdsprachiger Text. Das @xml:lang gibt die Sprache an, @re" [hi](hi.md) "Hervorhebung. Das @rend gibt die Art an (italic, bold, sup, " [ptr](ptr.md) "defines a pointer to another location." [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L" [rs](rs.md) "Referenzierende Zeichenkette für Akteure, die nicht als pers" [term](term.md) "Sachbegriff mit Verweis auf die Begriffs-Taxonomie via @ref " [title](title.md) "Titel mit verschiedenen Funktionen, unterschieden durch @typ"

**header:** [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer."

**namesdates:** [orgName](orgName.md) "Name einer Organisation mit Verweis auf die Meta-DB via @ref" [persName](persName.md) "Personenname mit Verweis auf die Meta-DB via @ref (kbga-acto" [placeName](placeName.md) "Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-I"

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
