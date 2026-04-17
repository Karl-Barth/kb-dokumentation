# `<body>` Textkörper

Enthält den gesamten Textkörper eines KBGA-Dokuments.

**Modul:** textstructure — Textstruktur

## Enthalten in

**textstructure:** [text](text.md) "enthält einen einzelnen, eigenständigen oder kompilierten Te"

## Content Model

```xml
<content>
  <sequence minOccurs="1" maxOccurs="1">
    <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
    <sequence minOccurs="0" maxOccurs="1">
      <classRef key="model.divTop"/>
      <alternate minOccurs="0" maxOccurs="unbounded">
        <classRef key="model.global"/>
        <classRef key="model.divTop"/>
      </alternate>
    </sequence>
    <sequence minOccurs="0" maxOccurs="1">
      <classRef key="model.divGenLike"/>
      <alternate minOccurs="0" maxOccurs="unbounded">
        <classRef key="model.global"/>
        <classRef key="model.divGenLike"/>
      </alternate>
    </sequence>
    <alternate minOccurs="1" maxOccurs="1">
      <sequence minOccurs="1" maxOccurs="unbounded">
        <classRef key="model.divLike"/>
        <alternate minOccurs="0" maxOccurs="unbounded">
          <classRef key="model.global"/>
          <classRef key="model.divGenLike"/>
        </alternate>
      </sequence>
      <sequence minOccurs="1" maxOccurs="unbounded">
        <classRef key="model.div1Like"/>
        <alternate minOccurs="0" maxOccurs="unbounded">
          <classRef key="model.global"/>
          <classRef key="model.divGenLike"/>
        </alternate>
      </sequence>
      <sequence minOccurs="1" maxOccurs="1">
        <sequence minOccurs="1" maxOccurs="unbounded">
          <alternate minOccurs="1" maxOccurs="1">
            <elementRef key="schemaSpec"/>
            <classRef key="model.common"/>
          </alternate>
          <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
        </sequence>
        <alternate minOccurs="0" maxOccurs="1">
          <sequence minOccurs="1" maxOccurs="unbounded">
            <classRef key="model.divLike"/>
            <alternate minOccurs="0" maxOccurs="unbounded">
              <classRef key="model.global"/>
              <classRef key="model.divGenLike"/>
            </alternate>
          </sequence>
          <sequence minOccurs="1" maxOccurs="unbounded">
            <classRef key="model.div1Like"/>
            <alternate minOccurs="0" maxOccurs="unbounded">
              <classRef key="model.global"/>
              <classRef key="model.divGenLike"/>
            </alternate>
          </sequence>
        </alternate>
      </sequence>
    </alternate>
    <sequence minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.divBottom"/>
      <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
    </sequence>
  </sequence>
</content>
```
