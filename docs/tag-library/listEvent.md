# `<listEvent>`

contains a list of descriptions, each of which provides information about an identifiable event.

[TEI Guidelines: listEvent](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listEvent.html)

**Modul:** namesdates — Namen und Daten

## Content Model

```xml
<content>
    <sequence>
      <classRef key="model.headLike" minOccurs="0" maxOccurs="unbounded"/>
      <elementRef key="desc" minOccurs="0" maxOccurs="unbounded"/>
      <alternate minOccurs="0" maxOccurs="unbounded">
        <elementRef key="relation" minOccurs="1" maxOccurs="1"/>
        <elementRef key="listRelation" minOccurs="1" maxOccurs="1"/>
      </alternate>
      <sequence minOccurs="1" maxOccurs="unbounded">
        <classRef key="model.eventLike" minOccurs="1" maxOccurs="unbounded"/>
        <alternate minOccurs="0" maxOccurs="unbounded">
          <elementRef key="relation" minOccurs="1" maxOccurs="1"/>
          <elementRef key="listRelation" minOccurs="1" maxOccurs="1"/>
        </alternate>
      </sequence>
    </sequence>
  </content>
```
