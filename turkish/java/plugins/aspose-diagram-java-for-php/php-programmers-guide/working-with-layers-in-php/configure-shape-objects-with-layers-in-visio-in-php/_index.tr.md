---
title: PHP'de Visio'de Şekil Nesnelerini Katmanlarla Yapılandırma
type: docs
weight: 10
url: /tr/java/configure-shape-objects-with-layers-in-visio-in-php/
---
## **Aspose.Diagram - Şekil Nesnelerini Katmanlarla Yapılandırma**
 Kullanarak Katmanlarla Şekil Nesnelerini Yapılandırmak İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**ShapeWithLayers'ı Yapılandır** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

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
## **Çalışan Kodu İndir**
 İndirmek**Visio'de (Aspose.Diagram) Katmanlarla Şekil Nesnelerini Yapılandırma**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithLayers/ConfigureShapeWithLayers.php)
