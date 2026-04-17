# `<abbr/>` (Abkürzung)

**Modul:** Kernmodule

## Beschreibung

Abkürzung mit Verweis auf das Abkürzungsverzeichnis via @ref.

## Erläuterung

Werden Abkürzungen stillschweigend aufgelöst, 
    sollte diese Vorgehensweise im TEI-Header über das editorialDecl-Element dokumentiert werden, 
    entweder in einem normalization- oder einem p-Element.

## Inhaltsmodell

- *macro.phraseSeq*

## Attribute

### `@type` (optional)

erlaubt es, die Abkürzung nach einer geeigneten Typologie zu klassifizieren.

**Datentyp:** teidata.enumerated

**Mögliche Werte:**

- `suspension` — die Abkürzung gibt nur den Anfang des Wortes oder der Phrase, der Rest wird weggelassen, z. B. H(ansestadt) H(amburg), u(nd) s(o) w(eiter).
- `contraction` — die Abkürzung lässt Buchstaben im Wortinneren weg.
- `brevigraph` — die Abkürzung verwendet ein spezielles Zeichen für die ausgelassenen Buchstaben.
- `superscription` — die Abkürzung enthält Zeichen auf oder über der Mittellinie.
- `acronym` — die Abkürzung besteht aus den Anfangsbuchstaben mehrer Wörter.
- `title` — eine Abkürzung für eine Anrede oder einen akademischen Titel (Dr., Hr., Fr., ...)
- `organization` — eine Abkürzung für den Namen einer Organisation.
- `geographic` — die Abkürzung steht für einen geografischen Namen.

## Beispiele

```xml
<abbr type="acron">CVJM</abbr>
```
