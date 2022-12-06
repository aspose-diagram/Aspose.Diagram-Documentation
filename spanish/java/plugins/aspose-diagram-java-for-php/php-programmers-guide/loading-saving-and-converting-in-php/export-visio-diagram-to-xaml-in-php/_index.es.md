---
title: Exportar Visio Diagram a XAML en PHP
type: docs
weight: 60
url: /es/java/export-visio-diagram-to-xaml-in-php/
---
## **Aspose.Diagram - Exportar Visio Diagram a XAML**
 Para exportar Visio Diagram a XAML usando**Aspose.Diagram Java para PHP** , simplemente invocar**Exportar a Xaml** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Save as XAML

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xaml", $saveFileFormat->XAML);

print "Exported visio diagram to XAML.".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Exportar Visio Diagram a XAML (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXaml.php)
