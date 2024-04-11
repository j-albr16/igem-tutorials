# CSS

## File erstellen

CSS-files können mit jedem einfachen Text-Editor erstellt werden.
Direkt in VSCode: in der Sidebar auf das Symbol für "new file" klicken.
Es empfiehlt sich, die Datei in VSCode zu bearbeiten, u.A. deshalb, weil diverse Befehle
automatisch vervollständigt werden.
Die Dateiendung lautet .css

## .css in .html einbringen

Navigiere in dein html-file.
Im head fügst du folgendes ein und ersetzt ... durch den Namen deiner .css

    <link rel="stylesheet" href="...">


## Schreibweise

#### Verändern von Taginhalten
Beispiel: alle Überschriften mit dem h1-Tag sollen in grüner Schrift erscheinen.
Hierfür kann folgendes in .css eingefügt werden:

    h1{color: rgb(31, 225, 9);}
 Auf die gleiche Art lassen sich die Inhalte aller anderen html-tags verändern.
Zu bedenken ist hierbei, dass die Änderung auf ALLE tags eines Elements angewendet wird.
Im Beispiel bedeutet dies, dass alle h1 Überschriften grün erscheinen werden.

#### ID nutzen
Der opening-tag eines html-elements kann mit einer id versehen werden
    h2 id="einzigartig"> ... </h2>
Diese kann in .css referenziert werden

    #einzigartig {color: ...}
Die Veränderungen beziehen sich in diesem Fall nur auf das Element mit der entsprechenden id.
Alle anderen Elemente der gleichen Sorte (in diesem Fall also alle anderen h2) bleiben unverändert.

#### Klassen erstellen
Eine Klasse zu erstellen bietet sich an, wenn ein bestimmter Style häufiger verwendet werden soll.
Möchte man bspw. häufiger in roter Schrift schreiben, lässt sich dies folgendermaßen umsetzen:
    .red {color: ...}
Um die Klasse red in html anzuwenden, wird die gleiche Schreibweise wie bei der id genutzt,
jedoch anstelle von "id" einfach "class" geschrieben.

    <p class="red"> Dieser Text ist rot </p>
    <p> Dieser Text ist nicht mehr rot. </p>
    <pre class="red"> Wenn dieser Text nicht rot ist, läuft etwas falsch. </pre>