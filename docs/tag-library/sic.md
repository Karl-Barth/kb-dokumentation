# `<sic/>` (Lateinisch für 'auf diese Weise', 'so')

**Modul:** Kernmodule

## Beschreibung

Markiert die fehlerhafte Stelle in der Druckausgabe (innerhalb von choice/sic/corr). Das @ed gibt die Ausgabe an (typisch: pga).

## Erläuterung

Ausführliche Dokumentation:

- [Textelemente > Korrektionen Der Druckausgabe](https://dokumentation.karl-barth.ch/textelemente/korrektionen-der-druckausgabe/)

## Inhaltsmodell

- *macro.paraContent*

## Beispiele

**Beispiel 1:**

```xml
I don't know, Juan. It's so far in the past now
      — how
<sic>we can</sic> prove or disprove anyone's theories?
```

**Beispiel 2:**

```xml
I don't know, Juan. It's so far in the past now
      — how
<choice>
  <sic>we can</sic>
  <corr>can we</corr>
</choice> prove or disprove anyone's theories?
```
