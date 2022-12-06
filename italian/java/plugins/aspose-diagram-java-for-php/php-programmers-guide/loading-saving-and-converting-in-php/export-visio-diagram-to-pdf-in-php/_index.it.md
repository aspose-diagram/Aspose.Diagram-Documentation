---
title: Esporta Visio Diagram in PDF in PHP
type: docs
weight: 40
url: /it/java/export-visio-diagram-to-pdf-in-php/
---
## **Aspose.Diagram - Esporta Visio Diagram in PDF**
 Per esportare Visio Diagram in PDF utilizzando**Aspose.Diagram Java per PHP** , semplicemente invocare**Esporta in PDF** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PDF file format

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.pdf", $saveFileFormat->PDF);

print "Exported visio diagram to pdf.".PHP_EOL;

{{< /highlight >}}
## **Scarica il codice in esecuzione**
Scarica**Esporta Visio Diagram in PDF (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToPdf.php)
