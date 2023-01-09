---
title: Imposta i dati di riempimento di Visio Shape in PHP
type: docs
weight: 130
url: /it/java/set-visio-shape-s-fill-data-in-php/
---
## **Aspose.Diagram - Imposta Visio Dati di riempimento della forma**
 Per impostare Visio Riempire i dati della forma utilizzando**Aspose.Diagram Java per Rubino** , semplicemente invocare**SetShapeFillData** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<sizeof($shapes->getCount())) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "rectangle" && $shape->getID() == 1) {

$shape->getFill()->getFillBkgnd()->setValue($diagram->getPages()->getPage(0)->getShapes()->getShape(0)->getFill()->getFillBkgnd()->getValue());

$shape->getFill()->getFillForegnd()->setValue("#ebf8df");

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeFillData.vdx",$saveFileFormat->VDX);

print "Set visio shape's fill data.".PHP_EOL;

}

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Imposta Visio Dati di riempimento della forma (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeFillData.php)
