---
title: Rufen Sie Visio Connector-Informationen in PHP ab
type: docs
weight: 50
url: /de/java/retrieve-visio-connectors-information-in-php/
---
## **Aspose.Diagram - Abrufen von Visio-Verbindungsinformationen**
 Abrufen von Visio Connector-Informationen mit**Aspose.Diagram Java für PHP** , einfach aufrufen**GetConnectorsInfo** Modul. Hier sehen Sie Beispielcode.

**PHP-Code**

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
## **Laufcode herunterladen**
 Download**Abrufen von Visio-Verbindungsinformationen (Aspose.Diagram)**von einer der unten genannten Social-Coding-Sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetConnectorsInfo.php)
