---
title: Hämta alla lager från Visio Diagram i PHP
type: docs
weight: 20
url: /sv/java/retrieve-all-layers-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Hämta alla lager**
 För att hämta alla lager med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**GetAllLayers** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Hämta alla lager från Visio Diagram (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithLayers/GetAllLayers.php)
