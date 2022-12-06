---
title: Exportera Visio Diagram till bild i PHP
type: docs
weight: 30
url: /sv/java/export-visio-diagram-to-image-in-php/
---
## **Aspose.Diagram - Exportera Visio Diagram till bild**
 För att exportera Visio Diagram till bild med hjälp av**Aspose.Diagram Java för PHP** , helt enkelt åberopa**ExportToImage** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PNG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.png", $saveFileFormat->PNG);

print "Exported visio diagram to PNG.".PHP_EOL;

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Exportera Visio Diagram till bild (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToImage.php)
