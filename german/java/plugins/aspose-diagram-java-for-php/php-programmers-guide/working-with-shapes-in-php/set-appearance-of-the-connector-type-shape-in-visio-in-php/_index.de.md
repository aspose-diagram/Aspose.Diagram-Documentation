---
title: Legen Sie das Erscheinungsbild der Konnektortypform in Visio in PHP fest
type: docs
weight: 100
url: /de/java/set-appearance-of-the-connector-type-shape-in-visio-in-php/
---
## **Aspose.Diagram – Legen Sie das Erscheinungsbild der Verbindertypform in Visio fest**
 So stellen Sie das Aussehen der Form des Verbindungstyps in Visio ein**Aspose.Diagram Java für PHP** , einfach aufrufen**SetShapeAppearance** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram =new Diagram($dataDir."Drawing.vsd");

\# Access a particular page

$page=$diagram->getPages()->getPage("Flow 1");

\# get a particular connector shape

$shape=$page->getShapes()->getShape(1);

\# set dynamic connector appearance

$connectorsTypeValue=new ConnectorsTypeValue();

$shape->setConnectorsType($connectorsTypeValue->STRAIGHT_LINES);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeAppearance.vdx",$saveFileFormat->VDX);

print "Set appearnce of the connector type shape.".PHP_EOL;

{{< /highlight >}}
## **Laufcode herunterladen**
 Download**Legen Sie das Erscheinungsbild der Verbindertypform in Visio (Aspose.Diagram) fest.**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeAppearance.php)
