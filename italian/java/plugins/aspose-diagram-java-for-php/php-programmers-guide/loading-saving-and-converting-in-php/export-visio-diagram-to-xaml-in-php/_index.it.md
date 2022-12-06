---
title: Export Visio Diagram to XAML in PHP
type: docs
weight: 60
url: /it/java/export-visio-diagram-to-xaml-in-php/
---
## **Aspose.Diagram - Export Visio Diagram to XAML**
To Export Visio Diagram to XAML using **Aspose.Diagram Java per PHP** , semplicemente invocare**ExportToXaml** modulo. Qui puoi vedere il codice di esempio.

**Codice PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Save as XAML

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xaml", $saveFileFormat->XAML);

print "Exported visio diagram to XAML.".PHP_EOL;

{{< /highlight >}}
## **Scarica il codice in esecuzione**
 Scarica**Export Visio Diagram to XAML (Aspose.Diagram)**da uno qualsiasi dei siti di social coding sotto indicati:

- [Git Hub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXaml.php)
