# `<teiHeader>` TEI-Header (elektronische Titelseite)

wird aus der Meta- und Registerdatenbank erzeugt und soll im XML nicht verändert werden (https://meta.karl-barth.ch)

Eines der wenigen Elemente, die verpflichtend für ein valides TEI-Dokument sind.

**Modul:** header — Header

## Enthalten in

**textstructure:** [TEI](TEI.md) "enthält ein einzelnes TEI-konformes Dokument, das aus einem "

## Kann enthalten

**header:** [fileDesc](fileDesc.md) "enthält die vollständige bibliografische Beschreibung einer " [revisionDesc](revisionDesc.md) "dokumentiert die Änderungen, die an der Datei vorgenommen wu"

## Constraints

**header-full-citation**
:   header-full: titleStmt sollte title[@type='citation_line_1'] enthalten (Phase full).

## Beispiele

```xml
<teiHeader>
    <fileDesc>
      <titleStmt>
        <title type="volume" n="vol-01">Karl Barth - Rudolf Bultmann. Briefwechsel 1911-1966</title>
        <title type="formal">Anhang Nr. 9</title>
        <title type="content">Karl Barth an Friedrich Gogarten</title>
        <title type="citation_line_1">Karl Barth an Friedrich Gogarten, 16. Juli 1928</title>
        <title type="citation_line_2">https://kbga.karl-barth.ch/texts/1119 (Stand:21. Dezember 2020)</title>
        <title type="citation_line_3">Druck: Anhang Nr. 9, in: Karl Barth-Gesamtausgabe. Karl Barth - Rudolf Bultmann. Briefwechsel 1911-1966, Zürich 1994, S. 227–229Karl Barth-Gesamtausgabe. Karl Barth - Rudolf Bultmann. Briefwechsel 1911-1966, Zürich 1994, S. 227–229</title>
      </titleStmt>
      <editionStmt>
        <edition>Digitale Karl Barth-Gesamtausgabe</edition>
        <sponsor>Schweizerische Akademie der Geistes- und Sozialwissenschaften (SAGW)</sponsor>
        <sponsor>Schweizerischer Nationalfonds (SNF)</sponsor>
        <sponsor>Karl Barth-Stiftung</sponsor>
      </editionStmt>
      <publicationStmt>
        <publisher>Karl Barth-Archiv</publisher>
        <pubPlace>Basel</pubPlace>
        <date when="2020">2020</date>
        <availability>
          <licence target="https://creativecommons.org/licenses/by-nc-nd/4.0/deed.de">Creative Commons BY-NC-ND</licence>
        </availability>
        <idno type="url">https://kbga.karl-barth.ch/texts/1119</idno>
      </publicationStmt>
      <sourceDesc>
        <!-- The printed Gesamtausgabe -->
        <bibl type="pga" xml:id="pga">
          <title type="volume">Karl Barth - Rudolf Bultmann. Briefwechsel 1911-1966</title>
          <title type="text">9</title>
          <author ref="kbga-actors-2151">Barth, Karl</author>
          <pubPlace>Zürich</pubPlace>
          <publisher>Theologischer Verlag</publisher>
          <date type="publication">1994</date>
          <biblScope unit="page">Pp. 227-229</biblScope>
          <!--position within a volume-->
          <biblScope unit="part">119</biblScope>
        </bibl>
        <!-- The first digital edition (data from xml and database) -->
        <bibl type="asp" xml:id="asp">
          <title type="edition">Princeton Barth Project edition</title>
          <title type="text">electronic edition of Karl Barth, Gesamtausgabe V.1, Karl Barth Rudolf Bultmann Briefwechsel 1911-1966, anhang letter 9</title>
          <author ref="kbga-actors-2151">Barth, Karl</author>
          <editor>James R. Adair, Jr.</editor>
          <editor>Timothy J. Finney</editor>
          <editor>Christian Kelm</editor>
          <pubPlace>Princeton</pubPlace>
          <publisher>Alexander Street Press</publisher>
          <date type="publication">2001</date>
        </bibl>
        <!-- Data from KBA (https://kba.anton.ch) -->
        <msDesc type="source" xml:id="kbga-sources-112" n="A" subtype="Vorlage_der_Edition">
          <msIdentifier>
            <repository>Karl Barth-Archiv</repository>
            <idno type="kba-objects-identifier">KBA 9228.117</idno>
            <altIdentifier>
              <idno type="URI">https://kba.anton.ch/objects/15757</idno>
            </altIdentifier>
            <altIdentifier>
              <idno type="kba-objects-id">kba-objects-15757</idno>
            </altIdentifier>
            <altIdentifier>
              <idno type="kbga-sources-id">kbga-sources-112</idno>
            </altIdentifier>
          </msIdentifier>
          <msContents>
            <msItem>
              <title>Karl Barth an Friedrich Gogarten</title>
              <docDate>
                <date type="creation" when="1928-07-16">16. Juli 1928</date>
              </docDate>
            </msItem>
          </msContents>
        </msDesc>
        <!-- we should provide more types: <bibl type="not-found-in-kba"></bibl> <bibl type="not-in-kba"></bibl>  -->
      </sourceDesc>
    </fileDesc>
    <profileDesc>
      <langUsage>
        <language ident="ger">German</language>
      </langUsage>
      <textClass>
        <keywords>
          <term>letter</term>
        </keywords>
      </textClass>
      <correspDesc>
        <correspAction type="sent">
          <persName ref="kbga-actors-2151">Barth, Karl</persName>
          <date when="1928-07-16">16. Juli 1928</date>
        </correspAction>
        <correspAction type="received">
          <persName ref="kbga-actors-137">Gogarten, Friedrich</persName>
        </correspAction>
      </correspDesc>
    </profileDesc>
    <revisionDesc>
      <change when="2020-12-21T13:24:23+01:00">teiHeader was automatically produced from the database 2020-12-21T13:24:23+01:00</change>
    </revisionDesc>
  </teiHeader>
```

## Content Model

```xml
<content>
  <sequence minOccurs="1" maxOccurs="1">
    <elementRef key="fileDesc"/>
    <classRef key="model.teiHeaderPart" minOccurs="0" maxOccurs="unbounded"/>
    <elementRef key="revisionDesc" minOccurs="0"/>
  </sequence>
</content>
```
