---
title: Ottieni i dati del collegamento ipertestuale Shape da un disegno Visio in PHP
type: docs
weight: 20
url: /it/java/get-shape-hyperlink-data-from-a-visio-drawing-in-php/
---
## **Aspose.Diagram - Ottieni dati collegamento ipertestuale forma**
Per ottenere i dati del collegamento ipertestuale Shape utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**GetShapeHyperlinkData** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "drawing.vdx");

\# Get a particular shape

$shape=$diagram->getPages()->getPage("Flow 1")->getShapes()->getShape(1);

$hyperlinks=$shape->getHyperlinks();

$i=0;

while ($i<(int)(string)$hyperlinks->getCount()) {

$hyperlink=$hyperlinks->get($i);

print "Address: " . (string)$hyperlink->getAddress()->getValue();

print "Sub Address: " . (string)$hyperlink->getSubAddress()->getValue();

print "Description: " . (string)$hyperlink->getDescription()->getValue();

$i+=1;

}

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Ottieni dati collegamento ipertestuale forma da un disegno Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHyperlinks/GetShapeHyperlinkData.php)
