# `<encodingDesc>` Beschreibung der Kodierung

dokumentiert das Verhältnis zwischen dem elektronischen Text und seiner Quelle oder den Quellen, von denen er sich ableitet.

[TEI Guidelines: encodingDesc](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-encodingDesc.html)

**Modul:** header — Header

## Content Model

```xml
<content>
    <alternate minOccurs="1" maxOccurs="unbounded">
      <classRef key="model.encodingDescPart"/>
      <classRef key="model.pLike"/>
    </alternate>
  </content>
```
