---
title: Export Visio Diagram to SVG in PHP
type: docs
weight: 50
url: /es/java/export-visio-diagram-to-svg-in-php/
---
## **Aspose.Diagram - Export Visio Diagram to SVG**
To Export Visio Diagram to SVG using **Aspose.Diagram Java para PHP** , simplemente invocar**Exportar a SVG** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as SVG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.svg", $saveFileFormat->SVG);

print "Exported visio diagram to SVG.".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Export Visio Diagram to SVG (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToSvg.php)
