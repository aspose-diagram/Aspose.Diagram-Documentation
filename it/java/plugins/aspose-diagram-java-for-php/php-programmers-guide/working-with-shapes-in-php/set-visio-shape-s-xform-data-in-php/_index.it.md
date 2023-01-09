---
title: Imposta i dati XForm di Visio Shape in PHP
type: docs
weight: 150
url: /it/java/set-visio-shape-s-xform-data-in-php/
---
## **Aspose.Diagram - Imposta i dati XForm di Visio Shape**
 Per impostare i dati XForm di Visio Shape utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**SetShapeXFormData** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Imposta Visio Dati XForm di Shape (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeXFormData.php)
