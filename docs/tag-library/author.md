# `<author/>` (Autor)

**Modul:** Kernmodule

## Beschreibung

Verfasserangabe im teiHeader. Das @ref verweist auf die Personen-ID in der Meta-DB.

## Erläuterung

Insbesondere wenn eine Katalogisierung auf Basis des TEI-Headers erfolgen soll, ist es ratsam
      einen Namen aus einer annerkannten Normdatei zu verwenden. Die Attribute key und
      ref können außerdem benutzt werden, um auf kanonische Informationen über
      einen Autor zu verweisen, etwa in einem Bibliothekskatalog oder einer Online-Ressource.
    Im Fall von Rundfunksendungen sollte dies Element benutzt werden, um den Namen der Firma oder
      der Sendergruppe zu notieren, welche diese Rundfunksendung verantwortet.
    Wo ein Autor unbekannt oder nicht angegeben ist, kann dieses Element Text wie z. B.
      Unbekannt oder Nicht angegeben beinhalten.
      Wenn die entsprechenden TEI-Module benutzt werden, kann das Element auch detaillierte
      Auszeichnungen für Namen von Personen, Organisationen oder Orten beinhalten - insbesondere
      wenn mehrere Namen vorhanden sind.

## Inhaltsmodell

- *macro.phraseSeq*

## Attribute

### `@ref` (optional)

**Datentyp:** teidata.pattern
