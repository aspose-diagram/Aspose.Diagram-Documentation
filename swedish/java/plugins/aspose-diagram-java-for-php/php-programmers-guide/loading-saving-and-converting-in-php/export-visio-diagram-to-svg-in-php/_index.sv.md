---
title: Exportera Visio Diagram till SVG i PHP
type: docs
weight: 50
url: /sv/java/export-visio-diagram-to-svg-in-php/
---
## **Aspose.Diagram - Exportera Visio Diagram till SVG**
 För att exportera Visio Diagram till SVG med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**ExportToSvg** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as SVG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.svg", $saveFileFormat->SVG);

print "Exported visio diagram to SVG.".PHP_EOL;

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Exportera Visio Diagram till SVG (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToSvg.php)
