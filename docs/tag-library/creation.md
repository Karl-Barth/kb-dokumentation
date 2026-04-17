# `<creation/>` (Entstehung)

**Modul:** Header

## Beschreibung

beinhaltet Informationen zur Entstehung eines Textes.

## Erläuterung

Das creation-Element kann dafür verwendet werden, Einzelheiten über die Entstehung eines Textes, 
          z. B. Entstehungszeit und Entstehungsort, zu dokumentieren, wenn diese von Interesse sind. 
          Es kann auch eine mehr oder weniger strukturierte Entstehungsgeschichte mit den einzelnen Bearbeitungs- und Revisionstufen 
          enthalten; diese sollten mithilfe des listChange-Elements ausgezeichnet werden. Das creation-Element darf 
          aber nicht mit dem publicationStmt-Element, das Zeit und Ort der Veröffentlichung verzeichnet, verwechselt werden.

## Inhaltsmodell

- Beliebiger Textinhalt
- `<listChange>`
- *model.limitedPhrase*
