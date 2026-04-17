# `<q/>` (in Anführungszeichen)

**Modul:** Kernmodule

## Beschreibung

enthält Material, das vom umgebenden Text durch 
    Anführungszeichen oder ähnliche Methoden abgesetzt ist. Die Abhebung kann beliebige Gründe 
    haben, wie z. B. direkte Rede, wiedergegebene Gedanken, Fachbegriffe, Jargon, Distanzierung 
    des Autors, Zitate aus anderen Texten, erwähnte aber nicht benutzte Passagen.

## Erläuterung

Das Element kann benutzt werden, um anzuzeigen, dass eine Textpassage sich vom umgebenden Text 
      unterscheidet - aus Gründen, die nicht näher spezifiziert werden. Wenn das Element in dieser 
      Weise benutzt wird, kann das q-Element als syntactic sugar 
      (d.h. vereinfachte Schreibweise) für das hi-Element mit einem entsprechenden 
      Wert im rend-Attribut gedacht werden.

Ausführliche Dokumentation:

- [Textstruktur > Gedichte](https://dokumentation.karl-barth.ch/textstruktur/gedichte/)

## Erlaubt in

**Kernmodule:** [`<cit>`](cit.md), [`<sp>`](sp.md)

## Inhaltsmodell

- *macro.specialPara*

## Attribute

### `@type` (optional, erweiterbare Werteliste)

kann verwendet werden, um anzuzeigen, ob die abgesetzte 
        Textpassage gesprochen oder gedacht wird, oder um sie auf andere Weise detaillierter zu beschreiben.

**Datentyp:** teidata.enumerated

**Mögliche Werte:**

- `spoken` — Wiedergabe gesprochener Sprache
- `thought` — Wiedergabe von Gedanken, z. B. eines inneren Monologes
- `written` — Zitat aus einer schriftlichen Quelle
- `soCalled` — Distanzierung des Autors
- `foreign`
- `distinct` — linguistisch hervorgehoben
- `term` — Fachbegriff
- `emph` — rhetorische Emphase
- `mentioned` — bezieht sich auf sich selbst, 
            nicht auf den üblichen Bezugspunkt
