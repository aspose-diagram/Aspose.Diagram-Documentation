---
title: Exportera Visio Diagram till XPS i PHP
type: docs
weight: 80
url: /sv/java/export-visio-diagram-to-xps-in-php/
---
## **Aspose.Diagram - Exportera Visio Diagram till XPS**
För att exportera Visio Diagram till XPS med**Aspose.Diagram Java för PHP** , helt enkelt åberopa**ExportToXps** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as XPS

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xps", $saveFileFormat->XPS);

print "Exported visio diagram to XPS.".PHP_EOL;

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Exportera Visio Diagram till XPS (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXps.php)
