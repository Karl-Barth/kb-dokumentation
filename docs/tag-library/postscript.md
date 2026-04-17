# `<postscript>`

enthält einen Nachtrag (Postskriptum), z. B. zu einem Brief.

[TEI Guidelines: postscript](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-postscript.html)

**Modul:** textstructure — Textstruktur

## Content Model

```xml
<content>
    <sequence>
      <alternate minOccurs="0" maxOccurs="unbounded">
	<classRef key="model.global"/>
	<classRef key="model.divTopPart"/>
      </alternate>
      <classRef key="model.common"/>
      <alternate minOccurs="0" maxOccurs="unbounded">
	<classRef key="model.global"/>
	<classRef key="model.common"/>
      </alternate>
      <sequence minOccurs="0" maxOccurs="unbounded">
	<classRef key="model.divBottomPart"/>
	<classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
      </sequence>
    </sequence>
  </content>
```
