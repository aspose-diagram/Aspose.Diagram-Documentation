---
title: Export Visio Diagram to HTML in PHP
type: docs
weight: 20
url: /it/java/export-visio-diagram-to-html-in-php/
---
## **Aspose.Diagram - Export Visio Diagram to HTML**
To Export Visio Diagram to HTML using **Aspose.Diagram Java per PHP** , semplicemente invocare**Esporta in Html** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as Html

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.html", $saveFileFormat->HTML);

print "Exported visio diagram to HTML.".PHP_EOL;

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Export Visio Diagram to HTML (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToHtml.php)
