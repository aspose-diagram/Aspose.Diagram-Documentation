---
title: Recupera le informazioni sulla forma Visio in PHP
type: docs
weight: 70
url: /it/java/retrieve-visio-shape-information-in-php/
---
## **Aspose.Diagram - Recupera Visio Informazioni sulla forma**
 Per recuperare Visio Informazioni sulla forma utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**Ottieni InfoForma** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing1.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

\# Display information about the shapes

print "Shape ID : " . (string)$shape->getID().PHP_EOL;

print "Name : " . (string)$shape->getName().PHP_EOL;

print "Master Shape : ".(string)$shape->getMaster()->getName().PHP_EOL;

$i += 1;

}

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Recupera Visio Informazioni sulla forma (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/GetShapeInfo.php)
