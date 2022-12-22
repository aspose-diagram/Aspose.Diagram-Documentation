---
title: PHP'de Bir Şeklin Konumunu Değiştirme
type: docs
weight: 10
url: /tr/java/change-the-position-of-a-shape-in-php/
---
## **Aspose.Diagram - Bir Şeklin Konumunu Değiştirme**
 Kullanarak Bir Şeklin Konumunu Değiştirmek İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**Şekil Konumunu Değiştir** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i = 0;

while ($i<(int)(string)$shapes->getCount()) {

$shape = $shapes->get($i);

if ($shape->getNameU() == "Process" && (int)(string)$shape->getID() == 2) {

$shape->move(1, 1);

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."ChangeShapePosition.vdx",$saveFileFormat->VDX);

print"Changed postion of a shape.".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Bir Şeklin Konumunu Değiştirme (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ChangeShapePosition.php)
