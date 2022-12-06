---
title: Ställ in Visio Shape's Line Data i PHP
type: docs
weight: 140
url: /sv/java/set-visio-shape-s-line-data-in-php/
---
## **Aspose.Diagram - Ställ in Visio Shape's Line Data**
 För att ställa in Visio Shapes linjedata med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**SetShapeLineData** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i=0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "rectangle" && (int)(string)$shape->getID() == 1) {

$shape->getLine()->getLineColor()->setValue($diagram->getPages()->getPage(0)->getShapes()->getShape(1)->getFill()->getFillForegnd()->getValue());

$shape->getLine()->getLineWeight()->setValue(0.07041666666666667);

$shape->getLine()->getRounding()->setValue(0.1);

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeLineData.vdx", $saveFileFormat->VDX);

print "Set visio shape's line data.".PHP_EOL;

}

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Ställ in Visio Shape's Line Data (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeLineData.php)
