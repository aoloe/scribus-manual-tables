# Tables in Scribus

Scribus hat zwar ein Tabellen-Werkzeug, es wird aber empfohlen, Tabellen als Bild oder Vektorgrafik aus Libreoffice Writer / Calc zu laden.

Einfache Tabellen können auch in Scribus mit Tabulatoren gestaltet werden.

## Importing tables into Scribus

Tabelle können als PNG oder -- falls Ghostscript installiert ist -- als PDF in einen Bildrahmen geladen werden.

SVG oder -- ab Scribus 1.5.x -- PDF können auch als Vektorgrafik importiert werden. Fall der Text nicht korrekt dargestellt wird, soll er zuerst in Kurven umgewandelt werden.

Libreoffice kann direkt -- oder über Umwege -- Tabellen als PNG, PDF oder SVN exportieren.

### Tabellen als Bild laden

Draft:
  * How-to export a table to png in LO writer / calc: short description + evt. screenshots

Das Bild kann dann wie gewöhnlich in ein Bildrahmen geladen werden.


### Tabellen als Vektorgrafik laden

Draft:
  * How-to export a table to svg in LO writer / calc: short description + evt. screenshots
  * How-to export a table to svg in LO writer / calc: short description + evt. screenshots
  * How to rework a table in inkscape
  * How to load a PDF in an image frame
  * How to import an SVG
  * How To import a PDF
  * How to outline the text (LO, Inkscape, Scribus)

## Tabellen als Tabulatoren

...

## The table tool

Scribus hat ein Tabellen-Werkzeug in der Toolbar. Er ist aber umständlich zu gebrauchen und die meisten feature, und es hat so wenige Features, dass es sich noch nicht lohnt Tabellen direkt in Scribus zu Gestalten.

>Falls du es doch probieren möchtest: veraltete Tutorials empfehlen Tabellen als Gruppe auszulösen. Das ist Falsch und wird die Tabelle in Textrahmen umwandeln.
>In 1.4.x können Zellen mit alt-Klick aktiviert werden. In 1.5.x können wie üblich angeklickt werden.

### Laufende Entwicklung

Die Tabellen wurden für Scribus 1.5.x komplett überarbeitet: die Grundlagen sind solid, der Werkzeug ist aber noch zu unvollständig und noch nicht reif für den produktive Einsatz.

Dieser Abschnitt beschreibt die Feature die bereits implementiert wurden.

### Tabelle bearbeiten

Man kann die Tabelle mittels Maus oder im Eigenschaftenfenster wie gewohnt vergrößern, verkleinern oder an die richtige Stelle im Dokument verschieben.\\
_Achtung:_ Im Gegensatz zu vorherigen Scribus-Versionen muß man analog zu Bildern die Tabelle dann mittels Rechtsklick an den Rahmen anpassen. Dies geschieht nicht automatisch.

Im Tab Tabelle kann man die Hintergrundfarbe und die Umrandung der Tabelle festlegen. Letzteres wirkt sich nicht auf die Rahmen der Zeilen, Spalten oder Zellen aus!

Mit einem Rechtsklick kann man Spalten und Zeilen zur Tabelle hinzufügen oder gleichmäßig verteilen. Im _Editiermodus_ kann man auch Zeilen oder Spalten entfernen.

### Text bearbeiten

Mit einem Doppelklick in eine Zelle der Tabelle kommt man in den _Editiermodus_ und kann den Text direkt einfügen und wie in [[einfuehrung:textrahmen|Textrahmen]] beschrieben bearbeiten.

## #Hintergrundfarbe (Zellen)

Im _Editiermodus_ kann man die Hintergrundfarbe einer Zelle bestimmen. Diese Einstellung überschreibt eine eventuelle Hintergrundfarbe der gesamten Tabelle.\\

_Note:_ Es ist (noch) nicht möglich, mehrere Zellen auszuwählen und ihre Hintergrundfarbe auf einmal zu ändern.

### Zellrahmen

{{ :einfuehrung:zellrahmen.png?300|}}

Auch hier gilt wie in den vorigen Versionen, daß sich 2 Zellen praktisch eine Rahmenlinie teilen. Da ein Hervorheben nicht mehr über den X, Y, Z - Reiter möglich ist, gibt es im Tab Tabelle die Möglichkeit über das Quadrat rechts auszuwählen, welche Linien in Stärke und Farbe geändert werden sollen. (Wobei bei gleicher Linienstärke die zuerst vorhandene Linie gilt, ansonsten die stärkere Linie.)\\
Es ist also auch hier keine gute Idee, benachbarten Zellen unterschiedliche Rahmen zu geben.

Und wie schon bei der Hintergrundfarbe ist es nicht möglich, mehrere Zellen gleichzeitig zu bearbeiten. Will man also z.B. eine Tabelle mit gelben Linien in der Stärke 2 pt (anstatt der Standard-Einstellung 1 pt und schwarz), muß man sowohl den Rahmen für die gesamte Tabelle als auch die Rahmen für jede einzelne Zelle bearbeiten. Beziehungsweise jede zweite Zelle, da ja die gelbe Linie dicker als die schwarze ist und somit diese überlagert. Bei einer Stärke von 1 pt wäre es tatsächlich jede Zelle.\\
Analog gilt das auch für unsichtbare Tabellen - also Tabellen ohne (sichtbaren) Rahmen.

## Beispiele

{{ :einfuehrung:tabelle146-seite001.png?420 |}}  
_Scribus 1.4.6_ Hintergrundfarbe Blau, einzelne Zellen eingefärbt, Spalte 2  über Eigenschaftenfenster mit schwarzen Linien versehen, alle anderen Rahmen ohne Farbe.\\

{{ :einfuehrung:table152-seite001.png?420 |}}  
_Scribus 1.5.2_ Hintergrundfarbe Blau, einzelne Zellen eingefärbt, jede einzelne Zelle und die gesamte Tabelle mit Rahmenlinie 0 pt und Farbe none versehen - außer die Zellen in Spalte 2, die rechts und links einen schwarzen Rahmen mit 3 pt bekamen.

## Authors: draft by laser and ale
