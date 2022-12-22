---
title: Uppdatera Visio Shape Text i PHP
type: docs
weight: 30
url: /sv/java/update-visio-shape-text-in-php/
---
## **Aspose.Diagram - Uppdatering Visio Formtext**
För att uppdatera Visio Forma text med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**UpdateShapeText** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i=0;

while($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "Process" && (int)(string)$shape->getID() == 1) {

$shape->getText()->getValue()->clear();

$shape->getText()->getValue()->add(new Txt("New Text"));

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."UpdateShapeText.vdx",$saveFileFormat->VDX);

print "Updated shape text.".PHP_EOL;

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Uppdatera Visio Formtext (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithText/UpdateShapeText.php)
