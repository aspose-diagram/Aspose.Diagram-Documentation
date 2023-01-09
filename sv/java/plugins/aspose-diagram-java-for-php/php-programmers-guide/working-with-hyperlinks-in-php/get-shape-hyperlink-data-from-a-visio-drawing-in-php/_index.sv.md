---
title: Få Shape Hyperlink Data från en Visio-ritning i PHP
type: docs
weight: 20
url: /sv/java/get-shape-hyperlink-data-from-a-visio-drawing-in-php/
---
## **Aspose.Diagram - Hämta Shape Hyperlink Data**
För att få Shape Hyperlink Data med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**GetShapeHyperlinkData** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "drawing.vdx");

\# Get a particular shape

$shape=$diagram->getPages()->getPage("Flow 1")->getShapes()->getShape(1);

$hyperlinks=$shape->getHyperlinks();

$i=0;

while ($i<(int)(string)$hyperlinks->getCount()) {

$hyperlink=$hyperlinks->get($i);

print "Address: " . (string)$hyperlink->getAddress()->getValue();

print "Sub Address: " . (string)$hyperlink->getSubAddress()->getValue();

print "Description: " . (string)$hyperlink->getDescription()->getValue();

$i+=1;

}

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Hämta Shape-hyperlänkdata från en Visio-ritning (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHyperlinks/GetShapeHyperlinkData.php)
