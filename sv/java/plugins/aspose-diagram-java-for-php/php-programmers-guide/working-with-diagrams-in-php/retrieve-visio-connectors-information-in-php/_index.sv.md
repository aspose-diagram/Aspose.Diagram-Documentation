---
title: Hämta Visio Anslutningsinformation i PHP
type: docs
weight: 50
url: /sv/java/retrieve-visio-connectors-information-in-php/
---
## **Aspose.Diagram - Hämta Visio Anslutningsinformation**
 För att hämta Visio Anslutningsinformation med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**GetConnectorsInfo** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$connectors = $diagram->getPages()->getPage(0)->getConnects();

$i = 0;

while ($i<sizeof($connectors->getCount())) {

$connector =$connectors->get($i);

\# Display information about the Connectors

print "From Shape ID : ".(string)$connector->getFromSheet().PHP_EOL;

print "To Shape ID : ".(string)$connector->getToSheet().PHP_EOL;

$i+=1;

}

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Hämta Visio Anslutningsinformation (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetConnectorsInfo.php)
