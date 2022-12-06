---
title: تكوين كائنات الشكل مع الطبقات في Visio في PHP
type: docs
weight: 10
url: /ar/java/configure-shape-objects-with-layers-in-visio-in-php/
---
## **Aspose.Diagram - تكوين كائنات الشكل بطبقات**
 لتكوين كائنات الشكل باستخدام الطبقات**Aspose.Diagram Java لـ PHP** ، ببساطة استدعاء**تكوين شكل مع طبقات** وحدة. هنا يمكنك أن ترى رمز المثال.

**كود PHP**

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
## **قم بتنزيل كود التشغيل**
 تحميل**تكوين كائنات الشكل مع الطبقات في Visio (Aspose.Diagram)**من أي من مواقع الترميز الاجتماعي المذكورة أدناه:

- [جيثب](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithLayers/ConfigureShapeWithLayers.php)
