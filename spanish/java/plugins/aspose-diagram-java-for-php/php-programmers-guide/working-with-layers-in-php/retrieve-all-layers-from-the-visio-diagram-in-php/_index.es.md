---
title: Recupere todas las capas del Visio Diagram en PHP
type: docs
weight: 20
url: /es/java/retrieve-all-layers-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Recuperar todas las capas**
 Para recuperar todas las capas usando**Aspose.Diagram Java para PHP** , simplemente invocar**ObtenerTodasLasCapas** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "Drawing.vsd");

\# get Visio page

$page=$diagram->getPages()->getPage(0);

$layers=$page->getPageSheet()->getLayers();

$i = 0;

while ($i<(int)(string)$layers->getCount()) {

$layer=$layers->get($i);

print "Name: " . (string)$layer->getName()->getValue();

print "Visibility: " . (string)$layer->getVisible()->getValue();

print "Status: " . (string)$layer->getStatus()->getValue();

$i += 1;

}

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Recuperar todas las capas del Visio Diagram (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithLayers/GetAllLayers.php)
