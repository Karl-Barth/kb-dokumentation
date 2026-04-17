# `<list>` Liste

Liste. Der @type unterscheidet geordnete und ungeordnete Listen.

Siehe [Textstruktur > Listen](https://dokumentation.karl-barth.ch/textstruktur/listen/)

[TEI Guidelines: list](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-list.html)

**Modul:** core — Kernmodule

## Attribute

**@type** (optional, erweiterbar)
:   beschreibt die Art der Listenpunkte.
:   Datentyp: teidata.enumerated
:   `gloss` — jeder Listenpunkt erläutert einen Begriff oder ein Konzept, das von einem voranstehenden label-Element genannt wird.
:   `index` — jeder Listenpunkt ist ein Registereintrag z. B. in einem alphabetisch geordneten 
                Sachregister am Ende einer Druckausgabe.
:   `instructions` — jeder Listenpunkt ist ein Arbeitsschritt in einer Folge von Anweisungen, 
                wie z. B. in einem Rezept.
:   `litany` — jeder Listenpunkt ist Teil einer Reihenfolge von Gebeten, Bitten oder Anrufungen die 
                üblicherweise in einem religiösen Ritual verwendet werden.
:   `syllogism` — jeder Listenpunkt ist Teil eines Arguments, das aus zwei oder mehr Prämissen 
                und einem daraus gezogenen Schluss besteht.

**@rend** (optional)


## Enthalten in

**header:** [keywords](keywords.md) "enthält eine Zusammenstellung von Schlagwörtern oder Phrasen" [revisionDesc](revisionDesc.md) "dokumentiert die Änderungen, die an der Datei vorgenommen wu"

## Kann enthalten

**core:** [item](item.md) "enthält einen Listenpunkt."

## Constraints

**gloss-list-must-have-labels**
:   The content of a "gloss" list should include a sequence of one or more pairs of a label element followed by an item element

## Beispiele

```xml
<div1 type="section">
    <head>Athelstan's Ordinance</head>
    <list rend="numbered">
      <item n="1">Concerning thieves. First, that no thief is to be spared who is caught with
            the stolen goods, [if he is] over twelve years and [if the value of the goods is] over
            eightpence. 
            <list rend="numbered">
          <item n="1.1">And if anyone does spare one, he is to pay for the thief with his
              wergild — and the thief is to be no nearer a settlement on that account — or to
              clear himself by an oath of that amount.</item>
          <item n="1.2">If, however, he [the thief] wishes to defend himself or to escape, he is
                not to be spared [whether younger or older than twelve].</item>
          <item n="1.3">If a thief is put into prison, he is to be in prison 40 days, and he may
                  then be redeemed with 120 shillings; and the kindred are to stand surety for him
                  that he will desist for ever.</item>
          <item n="1.4">And if he steals after that, they are to pay for him with his wergild,
                    or to bring him back there.</item>
          <item n="1.5">And if he steals after that, they are to pay for him with his wergild,
                      whether to the king or to him to whom it rightly belongs; and everyone of those who
                      supported him is to pay 120 shillings to the king as a fine.</item>
        </list>
      </item>
      <item n="2">Concerning lordless men. And we pronounced about these lordless men, from whom
            no justice can be obtained, that one should order their kindred to fetch back such a
            person to justice and to find him a lord in public meeting. 
            <list rend="numbered">
          <item n="2.1">And if they then will not, or cannot, produce him on that appointed day,
              he is then to be a fugitive afterwards, and he who encounters him is to strike him
              down as a thief.</item>
          <item n="2.2">And he who harbours him after that, is to pay for him with his wergild
                or to clear himself by an oath of that amount.</item>
        </list>
      </item>
      <item n="3">Concerning the refusal of justice. The lord who refuses justice and upholds
            his guilty man, so that the king is appealed to, is to repay the value of the goods and
            120 shillings to the king; and he who appeals to the king before he demands justice as
            often as he ought, is to pay the same fine as the other would have done, if he had
            refused him justice. 
            <list rend="numbered">
          <item n="3.1">And the lord who is an accessory to a theft by his slave, and it becomes
              known about him, is to forfeit the slave and be liable to his wergild on the first
              occasionp if he does it more often, he is to be liable to pay all that he owns.</item>
          <item n="3.2">And likewise any of the king's treasurers or of our reeves, who has been
                an accessory of thieves who have committed theft, is to liable to the same.</item>
        </list>
      </item>
      <item n="4">Concerning treachery to a lord. And we have pronounced concerning treachery to
            a lord, that he [who is accused] is to forfeit his life if he cannot deny it or is
            afterwards convicted at the three-fold ordeal.</item>
    </list>
  </div1>
```

## Content Model

```xml
<content>
  <sequence minOccurs="1" maxOccurs="1">
    <alternate minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.divTop"/>
      <classRef key="model.global"/>
      <elementRef key="desc" minOccurs="0" maxOccurs="unbounded"/>
    </alternate>
    <alternate minOccurs="1" maxOccurs="1">
      <sequence minOccurs="1" maxOccurs="unbounded">
        <elementRef key="item"/>
        <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
      </sequence>
      <sequence minOccurs="1" maxOccurs="1">
        <elementRef key="headLabel" minOccurs="0"/>
        <elementRef key="headItem" minOccurs="0"/>
        <sequence minOccurs="1" maxOccurs="unbounded">
          <elementRef key="label"/>
          <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
          <elementRef key="item"/>
          <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
        </sequence>
      </sequence>
    </alternate>
    <sequence minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.divBottom"/>
      <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
    </sequence>
  </sequence>
</content>
```
