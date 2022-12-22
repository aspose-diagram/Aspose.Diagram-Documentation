---
title: Recuperar información de conectores Visio en PHP
type: docs
weight: 50
url: /es/java/retrieve-visio-connectors-information-in-php/
---
## **Aspose.Diagram - Recuperar Visio Información de conectores**
 Para recuperar información de conectores Visio usando**Aspose.Diagram Java para PHP** , simplemente invocar**Obtener Información de Conectores** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Descargar código de ejecución**
 Descargar**Recuperar información de conectores Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetConnectorsInfo.php)
