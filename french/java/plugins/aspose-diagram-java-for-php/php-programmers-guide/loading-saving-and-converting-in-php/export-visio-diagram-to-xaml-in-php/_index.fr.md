---
title: Exporter Visio Diagram vers XAML en PHP
type: docs
weight: 60
url: /fr/java/export-visio-diagram-to-xaml-in-php/
---
## **Aspose.Diagram - Exporter Visio Diagram vers XAML**
 Pour exporter Visio Diagram vers XAML en utilisant**Aspose.Diagram Java pour PHP** , invoquez simplement**ExportToXaml** module. Ici vous pouvez voir un exemple de code.

**Code PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Save as XAML

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xaml", $saveFileFormat->XAML);

print "Exported visio diagram to XAML.".PHP_EOL;

{{< /highlight >}}
## **Télécharger le code d'exécution**
 Télécharger**Exporter Visio Diagram vers XAML (Aspose.Diagram)**à partir de l'un des sites de codage social mentionnés ci-dessous :

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXaml.php)
