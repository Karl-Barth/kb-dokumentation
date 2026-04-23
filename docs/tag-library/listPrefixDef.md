# `<listPrefixDef>`

contains a list of definitions of prefixing schemes used in teidata.pointer values, showing how abbreviated URIs using each scheme may be expanded into full URIs.

[TEI Guidelines: listPrefixDef](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listPrefixDef.html)

**Modul:** header — Header

## Enthalten in

**header:** [encodingDesc](encodingDesc.md) "dokumentiert das Verhältnis zwischen dem elektronischen Text" [listPrefixDef](listPrefixDef.md) "contains a list of definitions of prefixing schemes used in "

## Kann enthalten

**header:** [listPrefixDef](listPrefixDef.md) "contains a list of definitions of prefixing schemes used in " [prefixDef](prefixDef.md) "defines a prefixing scheme used in teidata.pointer values,
 "

## Content Model

```xml
<content>
    <sequence>
      <elementRef key="desc" minOccurs="0" maxOccurs="unbounded"/>
        <alternate minOccurs="1" maxOccurs="unbounded">
          <elementRef key="prefixDef"/>
          <elementRef key="listPrefixDef"/>
        </alternate>
    </sequence>
   </content>
```
