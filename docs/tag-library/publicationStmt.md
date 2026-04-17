# `<publicationStmt/>` (Angaben zur Veröffentlichung)

**Modul:** Header

## Beschreibung

umfasst Angaben zu Veröffentlichung oder Vertrieb eines elektronischen oder sonstigen Textes.

## Erläuterung

Wenn die Angaben zur Veröffentlichung mehrere Mitglieder der Klassen model.publicationStmtPart.agency oder model.publicationStmtPart.detail  
          enthalten und nicht einen oder mehrere Absätze (p) bzw. unbestimmte Einheiten (ab), dann hat 
          die Reihenfolge der Elemente eine Bedeutung, auf die zu achten ist. So müssen Elemente, die Angaben über den Veröffentlichungsort, 
          die Adresse, den Identifikator, die Verfügbarkeit und das Veröffentlichungsdatum enthalten, auf den Namen des Verlags, des 
          Distributors oder der Freigabeinstanz folgen, und zwar möglichst in dieser Reihenfolge.

## Erlaubt in

**Header:** [`<fileDesc>`](fileDesc.md)

## Inhaltsmodell

- *model.publicationStmtPart.agency*
- *model.publicationStmtPart.detail*
- *model.pLike*
