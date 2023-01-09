---
title: PHP'de Visio Şekil Bilgisini Alın
type: docs
weight: 70
url: /tr/java/retrieve-visio-shape-information-in-php/
---
## **Aspose.Diagram - Visio Şekil Bilgisini Al**
 Kullanarak Visio Şekil Bilgisini Almak İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**ShapeInfo'yu Al** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing1.vsd");

$shapes = $diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

\# Display information about the shapes

print "Shape ID : " . (string)$shape->getID().PHP_EOL;

print "Name : " . (string)$shape->getName().PHP_EOL;

print "Master Shape : ".(string)$shape->getMaster()->getName().PHP_EOL;

$i += 1;

}

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Şekil Bilgisini Alın (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/GetShapeInfo.php)
