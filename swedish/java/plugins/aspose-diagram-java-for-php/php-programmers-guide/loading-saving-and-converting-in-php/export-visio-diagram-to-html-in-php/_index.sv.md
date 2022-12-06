---
title: Exportera Visio Diagram till HTML i PHP
type: docs
weight: 20
url: /sv/java/export-visio-diagram-to-html-in-php/
---
## **Aspose.Diagram - Exportera Visio Diagram till HTML**
För att exportera Visio Diagram till HTML med**Aspose.Diagram Java för PHP** , helt enkelt åberopa**ExportToHtml** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as Html

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.html", $saveFileFormat->HTML);

print "Exported visio diagram to HTML.".PHP_EOL;

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Exportera Visio Diagram till HTML (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToHtml.php)
