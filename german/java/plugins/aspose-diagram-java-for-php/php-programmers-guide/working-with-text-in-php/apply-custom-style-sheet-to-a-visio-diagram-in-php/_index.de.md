---
title: Benutzerdefiniertes Stylesheet auf Visio Diagram in PHP anwenden
type: docs
weight: 10
url: /de/java/apply-custom-style-sheet-to-a-visio-diagram-in-php/
---
## **Aspose.Diagram - Anwenden eines benutzerdefinierten Stylesheets auf Visio Diagram**
 So wenden Sie ein benutzerdefiniertes Stylesheet auf eine Visio mit Diagram an**Aspose.Diagram Java für PHP** , einfach aufrufen**ApplyCustomStyleSheet** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes =$diagram->getPages()->getPage(0)->getShapes();

$i=0;

while ($i<(int)(string)$shapes->getCount()) {

$shape=$shapes->get($i);

if($shape->getNameU()=="Process") {

$source_shape =$shape;

break;

}

$i+= 1;

}

\# Find the required style sheet

$stylesheets=$diagram->getStyleSheets();

$j=0;

while($j<(int)(string)$stylesheets->getCount()) {

$stylesheet=$stylesheets->get($j);

if($stylesheet->getName() == "Basic") {

$custom_stylesheet = $stylesheet;

break;

}

$j+= 1;

}

if ($source_shape!=null && $custom_stylesheet !=null) {

\# Apply text style

$source_shape->setTextStyle($custom_stylesheet);

\# Apply fill style

$source_shape->setFillStyle($custom_stylesheet);

\# Apply line style

$source_shape->setLineStyle($custom_stylesheet);

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."ApplyCustomStyleSheet.vdx", $saveFileFormat->VDX);

print "Applied custom stylesheet to a visio diagram.".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Benutzerdefiniertes Stylesheet auf Visio Diagram (Aspose.Diagram) anwenden**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithText/ApplyCustomStyleSheet.php)
