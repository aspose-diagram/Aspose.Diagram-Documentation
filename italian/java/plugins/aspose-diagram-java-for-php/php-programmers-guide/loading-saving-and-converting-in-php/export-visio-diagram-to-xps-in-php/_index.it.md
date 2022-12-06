---
title: Export Visio Diagram to XPS in PHP
type: docs
weight: 80
url: /it/java/export-visio-diagram-to-xps-in-php/
---
## **Aspose.Diagram - Export Visio Diagram to XPS**
To Export Visio Diagram to XPS using **Aspose.Diagram Java per PHP** , semplicemente invocare**ExportToXps** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as XPS

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xps", $saveFileFormat->XPS);

print "Exported visio diagram to XPS.".PHP_EOL;

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Export Visio Diagram to XPS (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXps.php)
