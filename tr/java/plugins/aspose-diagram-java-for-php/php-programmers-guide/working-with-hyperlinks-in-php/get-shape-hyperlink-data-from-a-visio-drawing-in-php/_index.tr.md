---
title: PHP'de Visio Çiziminden Şekil Köprü Verilerini Alın
type: docs
weight: 20
url: /tr/java/get-shape-hyperlink-data-from-a-visio-drawing-in-php/
---
## **Aspose.Diagram - Şekil Köprü Verilerini Al**
Kullanarak Şekil Köprü Verilerini Almak İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**GetShapeKöprüVerileri** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

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
## **Çalışan Kodu İndir**
 İndirmek**Visio Çiziminden (Aspose.Diagram) Shape Hyperlink Verilerini Alın**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHyperlinks/GetShapeHyperlinkData.php)
