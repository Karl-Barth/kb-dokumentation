# `<term/>` (Fachbegriff)

**Modul:** Kernmodule

## Beschreibung

enthält ein einzelnes Wort, Mehrworttermini 
        oder symbolische Bezeichnungen, die als Fachbegriffe verstanden werden.

## Erläuterung

Wenn dieses Element innerhalb eines index-Elements auftritt, so wird es als Lemma dieses 
          Index-Eintrags angesehen. An anderer Stelle wird es einfach als Auszeichnung eines Fachbegriffs gewertet.
          Das term-Element kann mit einem entsprechenden gloss-Element über sein ref-Attribut 
          verknüpft werden; alternativ kann die Verknüpfung auch über das target-Attribut am gloss-Element 
          hergestellt werden.
      
      
          Es wird keine Position im Theoriediskurs bezogen, ob Fachbegriffe atomare oder größere lexikalische Einheiten umfassen können; 
          das term-Element kann für jedwede dieser Einheiten eingesetzt werden. Weiterhin wird keine Definition von "Fachbegriff" 
          gegeben, sondern jeder praktische Einsatz sanktioniert.
      
      
          So wie auch andere Mitglieder der Attributklasse att.canonical können term-Elemente im 
          laufenden Text mit entsprechenden kanonischen Definitionen verknüpft werden; entweder mittels einer URI (über das 
          ref-Attribut) oder mittels eines speziellen Codes (über das key-Attribut).
          Da sich die Attribute target und cRef gegenseitig ausschließen und mit dem ref-Attribut überlappen, 
          sind diese als "veraltet" gekennzeichnet und können mit einer der folgenden Guideline-Auflagen entfernt werden.

## Erlaubt in

**Header:** [`<keywords>`](keywords.md)

## Inhaltsmodell

- *macro.phraseSeq*
