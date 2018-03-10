# Tables in Scribus

Scribus hat zwar ein Tabellen-Werkzeug, es wird aber empfohlen, Tabellen als Bild oder Vektorgrafik aus Libreoffice Writer / Calc zu laden.

Einfache Tabellen können auch in Scribus mit Tabulatoren gestaltet werden.

## Do you really need a table?

"A table is structured for organizing and displaying information, with data arranged in columns and rows. Information is displayed as text, using words and numbers, and grid lines may be present or not. Sometimes it is best to remove the grid lines to ensure your table is easy to read and effective at communicating your message." (https://infogram.com/blog/do-you-know-when-to-use-tables-vs-charts/)

"Data visualization expert and author Stephen Few explains in his book, Show Me the Numbers: Designing Tables and Graphs to Enlighten – Second Edition, the times when a table makes the most sense:

The display will be used to look up individual values.
It will be used to compare individual values but not entire series of values to one another.
Precise values are required.
The quantitative information to be communicated involves more than one unit of measure.
Both summary and detail values are included." (https://infogram.com/blog/do-you-know-when-to-use-tables-vs-charts/)

```
Salesperson Jan Feb Mar
Jenny   3,565   4,333   6,123
John    7,899   8,040   9,300
Robert  2,345   3,453   3,056
Laura   10,005  10,800  9,898
Erika   5,200   6,453   5,100
TOTAL   $29,014 $33,079 $33,477
```

does it look like a good example to you?

Wouldn't this be much readable?

---> line chart: http://forums.scribus.net/index.php/topic,2858.msg13295.html#msg13295

sadly, i don't really agree with their table example. at least not in the context of scribus.

in my eyes, if there are interesting values about the salespersons, they should go in the text.
i don't see much value in putting that "static" table in the document.
imo, before publishing those numbers, one should think about the message to be conveyed.
in this specific case, probably, the focus is on the evolution of each person's sales through the months.
then something like the attached chart is much more expressive.

i agree with the author of the article, that sometimes you want to provide the raw data to your readers.
but that raw data is something that should go in a (linked, online) spreadsheet or -- eventually -- in the annexes.
the reader should be able to interactively "play" with it and we have nowadays tools for doing that.
(hey we have jupyter nowadays!)

the more i think about it, and the less i'm convinced that there are reasons for putting tables in a layout document...
except the laziness of the author : - )

my position: the tabulator are often enough, and if they are not, the data is probably better presented as a chart.

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


## Tables in Scribus: The short version

The standard hint: don't do table in Scribus:

- Tables are not a good way to provide information: try to avoid them (charts are way better!).
- Tabulators often produce a nicer (and simpler to read) layout.
- And if you really think you need a table, create it in libre office and import it as png, pdf, or svg (depending on the table and the scribus version).

The best formats for importing tables (and charts) are:

- PNG, it works with every version of scribus and office. you're importing a bitmap, of course, but it most cases it's good enough. just make sure, that the PNG is at the right size.
  - SVG: can work in both 1.4 and 1.6 and you get vectors. but you have to make sure that all features in the SVG are suported by scribus. and the text will be converted to paths.
    - PDF: can be imported as bitmap in 1.4 and and as bitmap, vector in an image frame (with limitations) and as vector (with text converted to paths.

You can use any image format that is supported by for export from office and for import in scribus, but those are probably the best options.
