---
title: Export Visio Diagram to XPS in PHP
type: docs
weight: 80
url: /es/java/export-visio-diagram-to-xps-in-php/
---
## **Aspose.Diagram - Export Visio Diagram to XPS**
To Export Visio Diagram to XPS using **Aspose.Diagram Java para PHP** , simplemente invocar**Exportar aXps** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as XPS

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.xps", $saveFileFormat->XPS);

print "Exported visio diagram to XPS.".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Export Visio Diagram to XPS (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXps.php)
