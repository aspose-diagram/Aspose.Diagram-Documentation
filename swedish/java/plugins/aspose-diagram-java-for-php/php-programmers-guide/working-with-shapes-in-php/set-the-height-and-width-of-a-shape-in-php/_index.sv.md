---
title: Ställ in höjd och bredd på en form i PHP
type: docs
weight: 120
url: /sv/java/set-the-height-and-width-of-a-shape-in-php/
---
## **Aspose.Diagram - Ställ in höjd och bredd på en form**
 För att ställa in höjd och bredd på en form med**Aspose.Diagram Java för PHP** , helt enkelt åberopa**SetShapeHeightAndWidth** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i=0;

while ($i <sizeof($shapes->getCount())) {

$shape = $shapes->get($i);

if ((string)$shape->getNameU()=="Process" && (int)(string)$shape->getID()==1) {

$shape->setWidth(2 * (int)(string)$shape->getXForm()->getWidth()->getValue());

$shape->setHeight(2 * (int)(string)$shape->getXForm()->getHeight()->getValue());

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeHeightAndWidth.vdx",$saveFileFormat->VDX);

print "Set height and width of shape.".PHP_EOL;

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Ställ in höjd och bredd på en form (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeHeightAndWidth.php)
