---
title: Recupera tutti i livelli da Visio Diagram in PHP
type: docs
weight: 20
url: /it/java/retrieve-all-layers-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Recupera tutti i livelli**
 Per recuperare tutti i livelli utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**Ottieni tutti i livelli** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "Drawing.vsd");

\# get Visio page

$page=$diagram->getPages()->getPage(0);

$layers=$page->getPageSheet()->getLayers();

$i = 0;

while ($i<(int)(string)$layers->getCount()) {

$layer=$layers->get($i);

print "Name: " . (string)$layer->getName()->getValue();

print "Visibility: " . (string)$layer->getVisible()->getValue();

print "Status: " . (string)$layer->getStatus()->getValue();

$i += 1;

}

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Recupera tutti i livelli da Visio Diagram (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithLayers/GetAllLayers.php)
