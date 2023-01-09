---
title: Hämta Masters Information i PHP
type: docs
weight: 30
url: /sv/java/retrieve-the-masters-information-in-php/
---
## **Aspose.Diagram - Hämta Masters Information**
 För att hämta Masters Information med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**GetMasterInfo** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir . "drawing.vsd");

$masters = $diagram->getMasters();

$i = 0;

while ($i<sizeof($masters->getCount())){

$master = $masters->get($i);

print "Master ID : " . (string)$master->getID().PHP_EOL;

print "Master Name : " . (string)$master->getName().PHP_EOL;

$i += 1;

}

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Hämta Masters Information (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterInfo.php)
