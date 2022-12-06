---
title: Recupera le informazioni sui connettori Visio in PHP
type: docs
weight: 50
url: /it/java/retrieve-visio-connectors-information-in-php/
---
## **Aspose.Diagram - Recupera Visio Informazioni sui connettori**
 Per recuperare le informazioni sui connettori Visio utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**GetConnectorsInfo** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

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
## **Scarica il codice in esecuzione**
 Scarica**Recupera le informazioni sui connettori Visio (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetConnectorsInfo.php)
