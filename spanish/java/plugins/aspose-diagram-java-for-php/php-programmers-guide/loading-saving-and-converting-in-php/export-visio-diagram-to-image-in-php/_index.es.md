---
title: Exportar Visio Diagram a Imagen en PHP
type: docs
weight: 30
url: /es/java/export-visio-diagram-to-image-in-php/
---
## **Aspose.Diagram - Exportar Visio Diagram a imagen**
 Para exportar Visio Diagram a imagen usando**Aspose.Diagram Java para PHP** , simplemente invocar**Exportar a imagen** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Save as PNG

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."Diagram.png", $saveFileFormat->PNG);

print "Exported visio diagram to PNG.".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Exportar Visio Diagram a Imagen (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/LoadingSavingandConverting/ExportToImage.php)
