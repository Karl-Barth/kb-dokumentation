# `<q>`
*in Anführungszeichen*

enthält Material, das vom umgebenden Text durch 
    Anführungszeichen oder ähnliche Methoden abgesetzt ist. Die Abhebung kann beliebige Gründe 
    haben, wie z. B. direkte Rede, wiedergegebene Gedanken, Fachbegriffe, Jargon, Distanzierung 
    des Autors, Zitate aus anderen Texten, erwähnte aber nicht benutzte Passagen.

!!! note "Dokumentation"
    - [Gedichte](https://dokumentation.karl-barth.ch/textstruktur/gedichte/)

**Modul:** core

## Attribute

| Attribut | Beschreibung | Werte |
|----------|-------------|-------|
| `@type` | kann verwendet werden, um anzuzeigen, ob die abgesetzte 
        Textpassage gesprochen oder gedacht wird, oder um sie auf andere Weise detaillierter zu beschreiben. | `spoken`, `thought`, `written`, `soCalled`, `foreign`, `distinct`, `term`, `emph`, `mentioned` (erweiterbar) |

### `@type`

- **`spoken`**: Wiedergabe gesprochener Sprache
- **`thought`**: Wiedergabe von Gedanken, z. B. eines inneren Monologes
- **`written`**: Zitat aus einer schriftlichen Quelle
- **`soCalled`**: Distanzierung des Autors
- **`distinct`**: linguistisch hervorgehoben
- **`term`**: Fachbegriff
- **`emph`**: rhetorische Emphase
- **`mentioned`**: bezieht sich auf sich selbst, 
            nicht auf den üblichen Bezugspunkt

## Content-Model

macro.specialPara
