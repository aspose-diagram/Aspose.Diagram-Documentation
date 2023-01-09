---
title: Obtenga datos de hipervínculo de forma de un dibujo Visio en PHP
type: docs
weight: 20
url: /es/java/get-shape-hyperlink-data-from-a-visio-drawing-in-php/
---
## **Aspose.Diagram - Obtener datos de hipervínculo de forma**
Para obtener datos de hipervínculo de forma usando**Aspose.Diagram Java para PHP** , simplemente invocar**GetShapeHyperlinkData** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "drawing.vdx");

\# Get a particular shape

$shape=$diagram->getPages()->getPage("Flow 1")->getShapes()->getShape(1);

$hyperlinks=$shape->getHyperlinks();

$i=0;

while ($i<(int)(string)$hyperlinks->getCount()) {

$hyperlink=$hyperlinks->get($i);

print "Address: " . (string)$hyperlink->getAddress()->getValue();

print "Sub Address: " . (string)$hyperlink->getSubAddress()->getValue();

print "Description: " . (string)$hyperlink->getDescription()->getValue();

$i+=1;

}

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Obtener datos de hipervínculo de forma de un dibujo Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHyperlinks/GetShapeHyperlinkData.php)
