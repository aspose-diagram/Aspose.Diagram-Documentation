---
title: Exportar Visio Diagram a XPS en PHP
type: docs
weight: 80
url: /es/java/export-visio-diagram-to-xps-in-php/
---
## **Aspose.Diagram - Exportar Visio Diagram a XPS**
 Para exportar Visio Diagram a XPS usando**Aspose.Diagram Java para PHP** , simplemente invocar**Exportar aXps** módulo. Aquí puedes ver el código de ejemplo.

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
 Descargar**Exportar Visio Diagram a XPS (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToXps.php)
