# `<q/>` (in Anführungszeichen)

**Modul:** Kernmodule

## Beschreibung

enthält Material, das vom umgebenden Text durch 
    Anführungszeichen oder ähnliche Methoden abgesetzt ist. Die Abhebung kann beliebige Gründe 
    haben, wie z. B. direkte Rede, wiedergegebene Gedanken, Fachbegriffe, Jargon, Distanzierung 
    des Autors, Zitate aus anderen Texten, erwähnte aber nicht benutzte Passagen.

!!! note "Ausführliche Dokumentation"
    [Textstruktur > Gedichte](https://dokumentation.karl-barth.ch/textstruktur/gedichte/)


## Inhaltsmodell

- *macro.specialPara*

## Attribute

### `@type` (erweiterbare Werteliste)

kann verwendet werden, um anzuzeigen, ob die abgesetzte 
        Textpassage gesprochen oder gedacht wird, oder um sie auf andere Weise detaillierter zu beschreiben.

**Datentyp:** `teidata.enumerated`

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
