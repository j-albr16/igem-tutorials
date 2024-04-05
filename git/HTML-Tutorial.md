# Grundlagen

Browser nutzen HTML als ihre Sprache 
Ein HTML Dokument ist immer nach einem gleich bleibenden Schema aufgebaut: 

Ein Dokument besteht immer aus sogenannten Tags, diese bestehen immer aus einem Anfang: 
<>
Und einem Ende 
</>
Ein Tag kann von Überschriften bis zu Text zu Bildern alles beinhalten. Dazu aber später mehr. 

## Basics 

1. Als allererstes muss der **Dokumenttyp** klassifiziert werden: 
```bash
<!DOCTYPE html>
``` 
2. Daraufhin startet das richtige **HTML Dokument**, was auch wiederum beschrieben werden muss: 
```bash
<html>
```
3. Jz kann man anfangen Spaß mit der Website zu haben: 

- Als erstes kann man der Website einen **Titel** geben (das, was im Browser oben in der Registerkarte angezeigt wird): 
```bash
<title> Titel </title>
```
- Daraufhin kann man den Body des Dokuments definieren, das ist der **sichtbare Teil** des Dokuments 
```bash
<body> 
```

- Ein guter Text brauch natürlich eine **Überschrift**: 
```bash
<h1> Überschrift </h1>
```
HTML Dokumente haben 6 mögliche Überschriften, die sich in Größe unterscheiden, definiert als h1-h6. 

- Die eigentlichen **Texte** werden als Paragraphen definiert: 
<p> Text </p> 

4. Desweiteren gibt es noch schöne kleine Tags, die nice to know sind: 
- **Zeilenumbruch**, das ist ein leeres Element, welches keinen Endtag hat
```bash
<br>
```
## Links 
Können auch in Websites eingebettet werden 
```bash
<a> 
```
Bei **Hyper-Links** muss auch noch die URL angegeben werde, diese wird durch ein Attribut näher definiert, dazu später mehr. 
Die URL wird dann so mit eingefügt. Durch das Einfügen eines Textes hinter die URL kann der Hyperlink noch beschriftet werden
```bash
<a href="URL"> Text </a>
```
## Bilder 
Kann man auch hochladen: 
```bash
<img>
```
Bei Bilder kommt immernoch die Quelle mit dazu, die über das src Attribut angegeben wird. Das kann natürlich einfach eine Datei auf dem PC sein, bei der man dann den Pfad angeben muss oder aber auch einfach nen Link. So ein Bild hat natürlich immer auch noch eine bestimmte Größe, auch das kann man mittels HTML definieren. Dafür kann man zwei weitere Attribute, neben dem src Attribut ergänzen: width (Breite); height (Höhe). Hinter das Attribut muss eine Pixelzahl geschrieben werden 
```bash
<img src="Quelle" width="500" height="500"> 
```
Außerdem gibt es noch ein weiteres Attribut für Bilder, sollten diese nicht richtig angezeigt werden können, wird ein alternativer Text angezeigt: 
```bash
<img src="Quelle" width="500" height="500" alt="Bild mit Bäumen"> 
```
