---
title: Esporta Visio Diagram in XPS in PHP
type: docs
weight: 80
url: /it/java/export-visio-diagram-to-xps-in-php/
---
## **Aspose.Diagram - Esporta Visio Diagram in XPS**
 Per esportare Visio Diagram in XPS utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**ExportToXps** modulo. Qui puoi vedere il codice di esempio.

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
 Scarica**Esporta Visio Diagram in XPS (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXps.php)
