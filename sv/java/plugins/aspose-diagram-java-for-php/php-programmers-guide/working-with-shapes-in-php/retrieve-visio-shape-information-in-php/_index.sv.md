---
title: Hämta Visio Shape Information i PHP
type: docs
weight: 70
url: /sv/java/retrieve-visio-shape-information-in-php/
---
## **Aspose.Diagram - Hämta Visio Forminformation**
 För att hämta Visio Forminformation med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**GetShapeInfo** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing1.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

\# Display information about the shapes

print "Shape ID : " . (string)$shape->getID().PHP_EOL;

print "Name : " . (string)$shape->getName().PHP_EOL;

print "Master Shape : ".(string)$shape->getMaster()->getName().PHP_EOL;

$i += 1;

}

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Hämta Visio Forminformation (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/GetShapeInfo.php)
