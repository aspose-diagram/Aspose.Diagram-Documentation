---
title: Ruota una forma con un angolo adatto in PHP
type: docs
weight: 80
url: /it/java/rotate-a-shape-with-suitable-angle-in-php/
---
## **Aspose.Diagram - Ruota una forma con un angolo adatto**
 Per ruotare una forma con un angolo adatto usando**Aspose.Diagram Java per PHP** , semplicemente invocare**Ruota Forma** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Ruota una forma con l'angolo adatto (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/RotateShape.php)
