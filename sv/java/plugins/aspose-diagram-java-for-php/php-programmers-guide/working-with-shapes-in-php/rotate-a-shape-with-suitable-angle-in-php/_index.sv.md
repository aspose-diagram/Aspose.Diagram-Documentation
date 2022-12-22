---
title: Rotera en form med lämplig vinkel i PHP
type: docs
weight: 80
url: /sv/java/rotate-a-shape-with-suitable-angle-in-php/
---
## **Aspose.Diagram - Rotera en form med lämplig vinkel**
 Att rotera en form med lämplig vinkel med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**Rotera form** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

\# Add a shape and set the angle

$diagram->getPages()->getPage(0)->getShapes()->getShape(1)->setAngle(190);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."RotateShape.vdx",$saveFileFormat->VDX);

print "Rotated shape.".PHP_EOL;

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Rotera en form med lämplig vinkel (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/RotateShape.php)
