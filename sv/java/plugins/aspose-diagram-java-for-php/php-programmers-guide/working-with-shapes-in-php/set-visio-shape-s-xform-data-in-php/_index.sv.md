---
title: Ställ in Visio Shapes XForm-data i PHP
type: docs
weight: 150
url: /sv/java/set-visio-shape-s-xform-data-in-php/
---
## **Aspose.Diagram - Ställ in Visio Shapes XForm-data**
 För att ställa in Visio Shapes XForm-data med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**SetShapeXFormData** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i=0;

while ($i<(int)(string)$shapes->getCount()){

$shape = $shapes->get($i);

if ($shape->getNameU()=="process" && $shape->getID() == 1) {

$shape->getXForm()->getPinX()->setValue(5);

$shape->getXForm()->getPinY()->setValue(5);

}

$i+= 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeXFormData.vdx",$saveFileFormat->VDX);

print "Set visio shape's XForm data.".PHP_EOL;

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Ställ in Visio Shapes XForm-data (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeXFormData.php)
