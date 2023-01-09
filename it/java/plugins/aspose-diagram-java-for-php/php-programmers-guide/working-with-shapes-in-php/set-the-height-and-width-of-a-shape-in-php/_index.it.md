---
title: Imposta l'altezza e la larghezza di una forma in PHP
type: docs
weight: 120
url: /it/java/set-the-height-and-width-of-a-shape-in-php/
---
## **Aspose.Diagram - Imposta l'altezza e la larghezza di una forma**
 Per impostare l'altezza e la larghezza di una forma utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**SetShapeHeightAndWidth** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Impostare l'altezza e la larghezza di una forma (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeHeightAndWidth.php)
