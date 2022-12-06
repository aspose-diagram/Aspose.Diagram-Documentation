---
title: Configurar objetos de forma con capas en Visio en PHP
type: docs
weight: 10
url: /es/java/configure-shape-objects-with-layers-in-visio-in-php/
---
## **Aspose.Diagram - Configurar objetos de formas con capas**
 Para configurar objetos de forma con capas usando**Aspose.Diagram Java para PHP** , simplemente invocar**ConfigurarFormaConCapas** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "Drawing.vsd");

$shapes = $diagram->getPages()->getPage("Flow 1")->getShapes();

$i = 0;

while ($i<(int)(string)$shapes->getCount()) {

$shape=$shapes->get($i);

#puts shape.getName().to_s

if ($shape->getName() == "Process") {

\# Add shape1 in first two layers. Here "0;1" are indexes of the layers

$layer = $shape->getLayerMem();

$layer->getLayerMember()->setValue("0;1");

}

elseif ($shape->getName()=="Preparation"){

\# Remove shape2 from all the layers

$layer = $shape->getLayerMem();

$layer->getLayerMember()->setValue("");

}

$i+=1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir . "Layers.vdx", $saveFileFormat->VDX);

print "Configured Shape Objects with Layers in Visio.".PHP_EOL;

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Configurar objetos de forma con capas en Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithLayers/ConfigureShapeWithLayers.php)
