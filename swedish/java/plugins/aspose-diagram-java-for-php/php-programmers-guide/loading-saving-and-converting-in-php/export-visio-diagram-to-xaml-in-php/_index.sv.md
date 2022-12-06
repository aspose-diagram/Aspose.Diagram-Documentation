---
title: Exportera Visio Diagram till XAML i PHP
type: docs
weight: 60
url: /sv/java/export-visio-diagram-to-xaml-in-php/
---
## **Aspose.Diagram - Exportera Visio Diagram till XAML**
För att exportera Visio Diagram till XAML med**Aspose.Diagram Java för PHP** , helt enkelt åberopa**ExportToXaml** modul. Här kan du se exempelkod.

**PHP-kod**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Save as XAML

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xaml", $saveFileFormat->XAML);

print "Exported visio diagram to XAML.".PHP_EOL;

{{< /highlight >}}
## **Ladda ner Running Code**
 Ladda ner**Exportera Visio Diagram till XAML (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXaml.php)
