---
title: Extrahieren Sie alle Bilder von einer Visio-Seite in PHP
type: docs
weight: 30
url: /de/java/extract-all-images-from-a-visio-page-in-php/
---
## **Aspose.Diagram - Extrahieren Sie alle Bilder von einer Visio-Seite**
 So extrahieren Sie alle Bilder von einer Visio-Seite mit**Aspose.Diagram Java für PHP** , einfach aufrufen**Bilder extrahieren** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

$shapes = $diagram->getPages()->getPage("Flow 1")->getShapes();

$i = 0;

$typeValue=new TypeValue();

while ($i <(int)(string)$shapes->getCount()){

$shape = $shapes->get($i);

\# Filter shapes by type Foreign

if ($shape->getType()== $typeValue->FOREIGN){

\# create an image file

$fos = new FileOutputStream($dataDir."Image#{i}.bmp");

$fos->write($shape->getForeignData()->getValue());

$fos->close();

}

$i += 1;

}

print "Extracted images successfully!".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Alle Bilder aus einer Visio-Seite extrahieren (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ExtractImages.php)
