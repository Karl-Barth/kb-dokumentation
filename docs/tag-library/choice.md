# `<choice>` Alternative

Gruppiert sic/corr-Paare für Korrekturen der Druckausgabe.

Siehe [Textelemente > Korrektionen Der Druckausgabe](https://dokumentation.karl-barth.ch/textelemente/korrektionen-der-druckausgabe/)

**Modul:** core — Kernmodule

## Attribute

**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


## Enthalten in

**core:** [choice](choice.md) "Gruppiert sic/corr-Paare für Korrekturen der Druckausgabe."

## Kann enthalten

**core:** [choice](choice.md) "Gruppiert sic/corr-Paare für Korrekturen der Druckausgabe."

## Beispiele

```xml
<choice>
    <sic source="pga">Ernst</sic>
    <corr resp="ak" type="corr">Emil</corr>
  </choice> Balla
```

## Content Model

```xml
<content>
  <alternate minOccurs="2" maxOccurs="unbounded">
    <classRef key="model.choicePart"/>
    <elementRef key="choice"/>
  </alternate>
</content>
```
