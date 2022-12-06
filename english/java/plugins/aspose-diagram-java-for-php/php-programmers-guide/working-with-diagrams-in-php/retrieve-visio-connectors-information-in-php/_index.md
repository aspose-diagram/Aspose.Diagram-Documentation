---
title: Retrieve Visio Connectors Information in PHP
type: docs
weight: 50
url: /java/retrieve-visio-connectors-information-in-php/
---

## **Aspose.Diagram - Retrieve Visio Connectors Information**
To Retrieve Visio Connectors Information using **Aspose.Diagram Java for PHP**, simply invoke **GetConnectorsInfo** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

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
## **Download Running Code**
Download **Retrieve Visio Connectors Information (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetConnectorsInfo.php)
