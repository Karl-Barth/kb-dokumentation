# `<ptr>`

defines a pointer to another location.

Die target und cRef-Attribute schließen sich gegenseitig aus.

Siehe [Textstruktur > Anmerkungen](https://dokumentation.karl-barth.ch/textstruktur/anmerkungen/)

[TEI Guidelines: ptr](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-ptr.html)

**Modul:** core — Kernmodule

## Attribute

**@n** (optional)

**@target** (optional)

**@type** (optional)

**@xml:id** (optional)


## Kann enthalten

Leeres Element.

## Constraints

**ptrAtts**
:   Only one of the attributes @target and @cRef may be supplied on .

## Content Model

```xml
<content>
  <empty/>
</content>
```
