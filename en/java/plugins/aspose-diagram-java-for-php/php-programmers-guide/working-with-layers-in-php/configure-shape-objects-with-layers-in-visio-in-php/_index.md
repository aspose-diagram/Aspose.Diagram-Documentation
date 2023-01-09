---
title: Configure Shape Objects with Layers in Visio in PHP
type: docs
weight: 10
url: /java/configure-shape-objects-with-layers-in-visio-in-php/
---

## **Aspose.Diagram - Configure Shape Objects with Layers**
To Configure Shape Objects with Layers using **Aspose.Diagram Java for PHP**, simply invoke **ConfigureShapeWithLayers** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

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
## **Download Running Code**
Download **Configure Shape Objects with Layers in Visio (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithLayers/ConfigureShapeWithLayers.php)
