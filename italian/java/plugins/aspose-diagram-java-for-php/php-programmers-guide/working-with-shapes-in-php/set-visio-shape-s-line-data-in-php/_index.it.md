---
title: Imposta i dati della linea di Visio Shape in PHP
type: docs
weight: 140
url: /it/java/set-visio-shape-s-line-data-in-php/
---
## **Aspose.Diagram - Set Visio Dati linea di Shape**
 Per impostare Visio Shape's Line Data utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**SetShapeLineData** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Imposta Visio Dati linea di forma (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeLineData.php)
