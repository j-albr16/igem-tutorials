# Grundlagen

Browser nutzen HTML als ihre Sprache 
Ein HTML Dokument ist immer nach einem gleich bleibenden Schema aufgebaut: 

Ein Dokument besteht immer aus sogenannten Tags, diese bestehen immer aus einem Anfang: 
<>
Und einem Ende 
</>
Ein Tag kann von Überschriften bis zu Text zu Bildern alles beinhalten. Dazu aber später mehr. 

Grob unterscheidet man noch in Inline Tags und in Block Tags. Letztere nehmen wie der Name schon suggeriert einen gesamten Block ein, was bedeutet, dass davor und danach eine Zeile freigelassen wird und der Block zusammenhängend formuliert wird. Block Elemente sind zum Beispiel: 
<p> --> Paragraph
<table> --> Tabelle
<li> --> Liste
Inline Tags sind Tags, die innerhalb eines Blocks stehen können, um diesen aufzuwerten mit Links, Bidern oder Zitaten zu versehen oder den Text stylisch aufzuwerten. Beispiele dafür wären. Diese haben keinen Absatz davor oder danach und können einfach in den bzw in einen Satz Block integriert werden. 
<a> --> Links 
<i> --> kursive Schrift 
<img> --> Bilder

## Basics 
Bevor wir mit dem eigentlichen HTML Tutorial loslegen, könht ihr einmal eine neue File bei Git erstelle und diese mit x.html bennen. Anhand dieser Datei können wir dann die Website modulieren. Wenn ihr als allererstes ein ! eingebt und den vorgeschlagenen Befehl auswählt, werden euch die gleich folgenden basics schon mal abgenommen ;) 

1. Als allererstes muss der **Dokumenttyp** klassifiziert werden. Den habt ihr da ja schon stehen durch das !, aber damit ihr wisst wofür das da ist ;) 
```bash
<!DOCTYPE html>
``` 
2. Daraufhin startet das richtige **HTML Dokument**, was auch wiederum beschrieben werden muss. Zwischen den beiden Tags steht ALLES was eure Website beinhalten drinne! Hier kann man
auch noch so Attribute ergänzen wie die **Sprache** eurer Website oder sowas schönes. Ein Beispiel dafür wäre:)  
```bash
<html lang="de"> 
</html>
```
3. Der **Head**:

Der Head macht so alles mögliche, was die gesamte Website betrifft, man kann die **Registerkarte** benennen, ein **Favicon** einfügen oder auch gesamte Klassen definieren. 
Man kann sich mittels CSS sytlisch austoben und ne Menge machen: 
- Als erstes definiert man die den Head der Website. Hier wird basically alles reingeschrieben, was global (also für die gesamte Website gelten soll): 
```bash 
<head> 
</head>
```
- Nun kann man der Website einen **Titel** geben, die Bezeichnung der Register Karte oben. Dieser Tag muss sich in dem <head> Tag befinden : 
```bash
<title> Probewebsite </title>
```
- Man kann neben diesem Titel auch noch ein **kleines Bildchen** (sogenanntes Favicon) darstellen lassen. Auch dieses muss in dem <head> Tag eingebettet sein. Die Quelle für das Bildchen muss hinter dem href stehen. Wofür der type steht wird euch bestimmt Jan besser erklären können. 
```bash 
<link rel="icon" type="image/x-icon" href="Quelle">
```
Erstellen kann man solche Flavicons zum Beispiel auf https://www.favicon.cc/. 
Damit es funktioniert hab ich einfach erstmal das Flavicon von Wikipedia geklaut: https://de.wikipedia.org/favicon.ico 

- Nun kann man auch noch mittels CSS Klassen definieren und oder bereits bestehende **Klassen** vordesignen. Dafür wir das CSS Attribute <style> verwendet. Hier befinden wir uns also 
nicht mehr nur bei HTML. Dazu erzählt Sunny euch gleich mehr. 

4. Daraufhin kann man den Body des Dokuments definieren, das ist der **sichtbare Teil** des Dokuments 
```bash
<body> </body>
```

- Ein guter Text braucht natürlich eine **Überschrift**: 
```bash
<h1> Überschrift </h1>
```
HTML Dokumente haben 6 mögliche Überschriften, die sich in Größe unterscheiden, definiert als h1-h6. H1 ist default am größten und h6 am kleinsten. 
Die Überschrift kann mittels Style Attributen noch mal angepasst werden. Diese sind auch wieder CSS propertys und dazu gleich von Sunny mehr.  

- In den meisten Fällen beginnt man nun damit einen neuen **Abschnitt** anzufangen, das wird über den <div> Tag definiert. Mittels CSS kann man den wiederum designen und Klassen zuordnen.
Da erzählt Sunny euch aber nachher noch mehr zu ;) 
```bash
<div> Text </div> 
```
Die eigentlichen **Texte** werden als Paragraphen definiert und sind Block Elemente: 
```bash
<p> Text </p> 
```
Bei dem eigentlichen Text gibt es viele interessante Anpassungen. Alles was zwischen den <p> </p> tags steht wird als zusammenhängender Text dargestellt. Manchmal möchte man das Ganze aber auch etwas anschaulicher gestalten: 
Mittels leeren Tags wie <hr> oder <br> können **thematische Umbrüche oder Zeilenümbrüche** dargestellt werden. 
```bash
<hr>
```
```bash
<br>
```

Bei dem Design der Paragraphen ist wichtig zu erwähnen, dass Leerzeichen oder Zeilenümbrüche mit Enter etc ignoriert werden. Je nach Bildschrim und Auflösung kann es also ohne das Nutzen von oben genannten Tags zu anderen Darstellungen des Texts kommen. Will man jz aber eine **vorher definierte Struktur** auch so angezeigt bekommmen, gibt es auch einen schönen Tag dafür: 
```bash
<pre> 
Dieser Text wird 
genauso 
dargestellt 
wie ich das hier schreibe 
</pre>
```
Im Vergleich dazu mit normalem Paragraph Tag:
```bash
<p> 
Dieser Text wird 
genauso 
dargestellt 
wie ich das hier schreibe 
</p>
```

5. Desweiteren gibt es noch schöne kleine Tags, die nice to know sind: 
## Links 
Können auch in Websites eingebettet werden 
```bash
<a> 
```
Bei **Hyper-Links** muss auch noch die URL angegeben werde, diese wird durch ein Attribut näher definiert, dazu später mehr. 
Die URL wird dann so mit eingefügt. Durch das Einfügen eines Textes hinter die URL kann der Hyperlink noch beschriftet werden. 
Eine beispielhafter Link wäre: https://www.notion.so/iGEM-2024-17116cb4ccda4210ab36a1d746f4b021 
```bash
<a href="URL"> unsere tolle Notion Page </a>
```
Man kann dem Link zusätzlich noch ein **Target** (wo der Spaß geöffnet wird) geben. Das Target wird noch mit in die <a> Klammer geschrieben und kommt hinter den href tag: 
    _self - Standard: wird im gleichen Tab/Fenster geöffnet, wie angeklickt 
    _blank - Link wird in neuem Tab oder Fenster geöffnet 
    _parent - Opens the document in the parent frame 
    _top - Opens the document in the full body of the window
```bash
<a href="https://www.notion.so/iGEM-2024-17116cb4ccda4210ab36a1d746f4b021" target="_blank"> Unsere Notion Page </a>
```
- Wenn man **Email Adressen** als Link darstellen möchte geht das natürlich man kann aber auch direkt dafür sorgen, dass sich das Email Programm der Person öffnet, dass es so einfach wie möglich wird eine Email an uns zu schreiben: 
```bash
<a href=mailto:"igem@uni-muenster.de"> Text </a>
```

Links aber auch alles andere können auch einen title erhalten, dieser wird dann beim drüberhovern als **Tool Tip** angezeigt und kann damit eine ganz schöne Ergänzung sein. 

```bash
<a href="URL" title="Damit kommt man zur Website"> Text </a>
```
Ein HTML Link kann nicht nu schnöde als Link angezeigt werden, sondern auch als **cooles Bild**. Dafür muss neben dem href Attribut in der <a> Klammer auch noch der img Tag dahinter gesetzt werden. Wie man Bilder vernünftig anzeigt wird weiter unten beschrieben. 
```bash
<a href="https://igem.org/"> 
<img src="https://static.igem.org/mediawiki/igem.org/3/3f/Igem-logo-fullcolorwhite%402x.png"> Text </a>
```
Um die Website ein bisschen einfacher zugänglich zu machen können **Bookmarks** erstellt werden, also ich klicke auf was drauf und springe direkt irgendwo hin. Diese Bookmarks müssen erst definiert werden. Das geschieht durch den id tag. Dann gibt man dem Bookmark einen Namen, der dann für den Link dahin entscheidend ist, also möglichst irgendwas einfaches: 
```bash
<h1 id="Ü1"> Diese Überschriftt ist so toll, dass man da immer wieder hin will</h1>
```
Danach muss nur noch ein Link erstellt werden, der dann zu dieser Überschrift/Kapitel führt 

```bash
<a href="#Ü1"> hier gehts wieder zu dieser wahnsinnig geilen Überschrift </a>
```
## Bilder 
Kann man auch hochladen: 
```bash
<img>
```
Bei Bilder kommt immernoch die Quelle mit dazu, die über das src Attribut angegeben wird. Das kann natürlich einfach eine Datei auf dem root directory sein, bei der man dann den Pfad angeben muss oder aber auch einfach nen Link. So ein Bild hat natürlich immer auch noch eine bestimmte Größe, auch das kann man mittels HTML definieren. Dafür kann man zwei weitere Attribute, neben dem src Attribut ergänzen: width (Breite); height (Höhe). Hinter das Attribut muss eine Pixelzahl geschrieben werden 
```bash
<img src="Quelle" width="500" height="500"> 
```
Außerdem gibt es noch ein weiteres Attribut für Bilder, sollten diese nicht richtig angezeigt werden können, wird ein alternativer Text angezeigt: 
```bash
<img src="Quelle" width="500" height="500" alt="Bild mit Bäumen"> 
```
Mittels dem Style Attribute kann man auch Bilder noch ein klein wenig aufpeppen. So kann man die Größe eines Bildes auch durch das style Attribut darstellen, was zumindest von der W3 School empfohlen wird oder man kann die Bilder an eine Seite alignen und so weiter. 


# Advanced
## Style Attribute 
Das Style Attribute ist mega cool, aber leider CSS, deswegen darf ich dazu nichts sagen und Sunny macht das nachher alles. 

## HTML Elemente 
### Text formatierende Elemente 
Auch hier mit kann man cooles Zeug machen, das sind dann auch richtige HTML Elemente und haben nichts mit CSS zu tun, wie die Style Attribute. Mit einer Auswahl an Elementen kann man seinen Text so auch anpassen. 

    <b> - Fettgedruckter Text
    <strong> - Wichtiger Text, der auch fettgedruckt dargestellt wird
    <i> - Kursiv
    <em> - Betonter Text, wird auch kursiv dargestellt ist aber vor allem für eine Sprachausgabe wichtig
    <mark> - markierter Text (gelb)
    <small> - Einfach kleiner Text
    <del> - Durchgestrichene
    <ins> - Unterstrichen
    <sub> - Tiefgestellt
    <sup> - Hochgestellt

Diese Elemente werden (im Gegensatz zu den style attributen) NICHT mit in die Klammer geschrieben, sondern stehen dahinter. Entscheidend dabei ist natürlich, dass auch diese Elemente einen Start und einen Endtag haben! Das sind INLINE Tags können also so einfach in den Text integriert werden. 

```bash
<p><b> Ich bin fettgedruckter Text </b> <del> und ich wurde durchgestrichen </del> </p> 
```
### Zitationen 
Für uns auch nicht von unentscheidender Bedeutung ist das wörtliche Zitieren auf unserer Website, auch wenn das indirekte Zitieren in der Biologie öfter verwendet wird: 
Auch hier gibt es wieder ganz unterschiedliche Elemente, die man sich zur Nutze machen kann. 

1. Blockqoute 
Hiermit wird dargestellt, dass ein **kompletter Block** von einer Quelle <blockquote> entnommen worden ist. Dargestellt wird das in der Website durch eine Einrückung des Textes. Für irgendeine Quelle muss natürlich die Quelle auch verlinkt werden, das wird durch den <cite> tagrealisiert: 
```bash
<blockquote cite:"Quelle">
```
2. kurze Zitate 
Der <q> Tag für Quotation steht für **kurze wörtliche Zitate** die in einen Paragraphen eingebettet werden können: 
```bash
<p>Ich bin normaler Text <q> Ich werde zitiert</q> hier geht der normale Text weiter </p>
```

3. Der Cite tag 
Mithilfe von diesem Tag lassen sich, wie oben dargestellt, Quellen für Zitate angeben. Dieser tag kann aber auch alleine stehen, wenn zum Beispiel ein **Buch Titel** oder sowas erwähnt wird. Der Inhalt zwischen dem Anfang und dem Endtag wird dann kursiv dargestellt: 
```bash
<cite> Titel meines Werkes </cite>
```

4. kleinere nicht sooo wichtige Tags 
- <abbr> Abkürzungen 
Mit diesem Tag kann man Wörter **abkürzen** lassen und zeitgleich das Ganze auch als abgekürtze Variante markieren. Angegeben wird zuerst die lange Version, gefolgt von der Abkürzung, damit der Browser auch weiß wie er das darstellen soll.  

```bash
<p> Der <abbr title="international genetic engineered machine"> iGEM </abbr> Wettbewerb wird dieses Jahr von Münster gewonnen </p>
```

- Mit dem <adress> tag lassen sich **Kontaktinformationen** darstellen. Diese werden im Browser dann kursiv geschrieben. 

- Bidirektionaler Text schreibt den Text von hinten nach vorne auf -> 5' - 3' : 
```bash
<bdo> Der Text wird jz von hinten nach vorne aufgeschrieben </bdo>
```

## Kommentare 
Auch kann man Kommentare darstellen, die dann nicht auf der eigentlichen Website angezeigt werden, wohl aber im Code zu finden sind. Damit lassen sich auch Sachen temporär verstecken oder sowas. Alles zwischen den Tags wird nicht auf der Website angezeigt: 
<! -- Ich bin ein Kommentar -->

## Inhaltliches 
- Neben reinem Text kann man mit HTML natürlich auch noch andere Sachen designen, wie bspw Tabellen. Diese werden mit dem <table> tag gestartet. Darauffolgend müssen die Zeilen der Tabelle hintereinander definiert werden, das geschieht über den <tr> tag für table row. Die erste Zeile einer Tabelle sind ja meistens die Überschriften. Diese werden mit dem <th> Tag versehen und werden dadurch fettgedruckt. Der th tag muss innerhabl des tr tags sein. Der Inhalt der einzelnen Blöcke wird dann innerhalb des tr tags mit dem <td> Tag definiert für table data. Das sieht dann bspw so aus: 
```bash 
<table> 
<tr>
<th> Überschrift 1 </th>
<th> Überschrift 2 </th>
</tr>
<tr>
<td> Inhalt 1 
<td> Inhalt 2 
</tr>
</table>
```
...
Um der Tabelle eine Überschrift zu geben wir der <caption> Tag verwendet. 
Neben diesen Tags gibt es auch noch ne Menge an stylischen Tags, die auch wieder alle CSS properties sind. 
```bash 
<table> 
<caption> Ich bin eine tolle Tabelle </caption>
<tr>
<th> Überschrift 1 </th>
<th> Überschrift 2 </th>
</tr>
<tr>
<td> Inhalt 1 
<td> Inhalt 2 
</tr>
</table>
```
- **Listen** sind auch ein gern gesehenes Tool auf Websiten. Für Listen gibt es zwei Tags. Eine normale bullted List wird mit dem <ul> Tag versehen für unorderd HTML List. Eine geordnete Liste mit Nummerierung wird durch den <ol> Tag definiert für ordered HTML List. 
Der Inhalt der Liste wird dann durch den <li> Tag definiert und ist sowohl für geordnete als auch ungeordnete Listen gleich. 
Als kleine Spezialversion gibt es noch eine Liste mit Beschreibungen, über den <dl> für description list tag beschrieben. Hier funktioniert die Aufzählung etwas anders. Die Sachen, die beschrieben werden  sollen, werden mit dem <dt> tag versehen. Darunter kommt die Beschreibung dafür mit dem <dd> tag. Bsp: 

```bash 
<dl>
<dt> iGEM 
<dd>ein cooles Projekt mit vielen Möglichkeiten 
<dt> Münster 
<dd> tolle Stadt 
<dt>2024 
<dd> ein Jahr 
</dl>
```

## Java Script 

Mit dem <script> 
Tag kann man beschreiben, dass als nächstes ein Java Script Element kommt. Entweder man schreibt eben dieses direkt in den script Tag rein oder man verweist mit dem <src> Tag auf ein externes Skript. 
Java Script braucht man beispielsweise für solche Elemente wie Input tags, wie mit dem Knopf oder der Eingabe des Namens oder auch das mit der Glühbirne. Auch recht einfache 
Befehle, aber dann habt ihr das schon mal gesehen ;) 
Für diese kleinen Sachen, wie beispielsweise der Namen und Nachmanem Input. Definiert man zuerst was quasi passieren soll, wenn interagiert wird: 
Das wird über den <form> tag und dem action attribute realsiert. Nach dem Action attribute kommt dann bspw eine Datei, die sich runterlädt oder es wird auf eine Website weitergeleitet oder so. 
```bash 
<form action="https://www.notion.so/iGEM-2024-17116cb4ccda4210ab36a1d746f4b021">
```
Danach muss man natürlich noch irwie gucken, dass man irwie was eingeben kann, das wird über die Kombination von <label> tags zum beschriften 
 ```bash 
<form action="https://www.notion.so/iGEM-2024-17116cb4ccda4210ab36a1d746f4b021">
<label> Name </label>
<input type="text"> 
<input type="submit" value="Bestätigung">
```
Oben beschriebens würde euch zu unserer Notion Website weiterleiten. 

## Semantik 
Ich habe ja jetzt schon viel über Paragraphen geredet. Diese und auch <div> Elemente geben keinen Aufschluss über den Inhalt des darin befindlichen Textes, diese Elemente sind nicht-semantisch. Es sind also ganz neutrale Text Tags. Wenn man nun aber schon ganz genau weiß was man für einen Inhalt hat und diesen auch als solchen definieren möchte bietet HTML eine gute Bandbreite an semantischen Tags dafür:

<article> 	Defines independent, self-contained content
<aside> 	Defines content aside from the page content
<details> 	Defines additional details that the user can view or hide
<figcaption> 	Defines a caption for a <figure> element
<figure> 	Specifies self-contained content, like illustrations, diagrams, photos, code listings, etc.
<footer> 	Defines a footer for a document or section
<header> 	Specifies a header for a document or section
<main> 	Specifies the main content of a document
<mark> 	Defines marked/highlighted text
<nav> 	Defines navigation links
<section> 	Defines a section in a document
<summary> 	Defines a visible heading for a <details> element
<time> 	Defines a date/time

Die lassen sich natürlich dann auch nochmal sehr gut mit CSS Stylen und anpassen und was auch immer, aber so kann man bereits in HTML eine gewisse Defintion an Content abgeben. 

## Entities 
Entities sind Zeichen und Symbole, die so nicht auf ner normalen Tastatur zu finden sind. Beispiele dafür sind mathematische Zeichen, Emojis. Diese werden entweder über ihre Nummer oder mit ihrem Namen eingefügt. Bspw am < Zeichen: 
```bash 
<p> Ich bin größer &gt; als der Spaß hier </p>
```
Eine sehr wichtige Entity ist wohl die non breaking space entity. Durch die man Zeilenumbrüche zwischen zwei wörtern oder so verhindern kann oder dadurch Zeilen einfügen kann, die der Browseer nicht zerstört. Mit den UTF-8 characters kann man aber gefühlt alles mögliche darstellen. Man muss nur den richtigen Codefür die Entity wissen 


