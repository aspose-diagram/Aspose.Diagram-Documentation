---
title: PHP'de Bir Şeklin Yüksekliğini ve Genişliğini Ayarlama
type: docs
weight: 120
url: /tr/java/set-the-height-and-width-of-a-shape-in-php/
---
## **Aspose.Diagram - Bir Şeklin Yüksekliğini ve Genişliğini Ayarla**
 Bir Şeklin Yüksekliğini ve Genişliğini Ayarlamak için**PHP için Aspose.Diagram Java** , sadece çağırmak**SetShapeHeightAndWidth** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

$shapes=$diagram->getPages()->getPage(0)->getShapes();

$i=0;

while ($i <sizeof($shapes->getCount())) {

$shape = $shapes->get($i);

if ((string)$shape->getNameU()=="Process" && (int)(string)$shape->getID()==1) {

$shape->setWidth(2 * (int)(string)$shape->getXForm()->getWidth()->getValue());

$shape->setHeight(2 * (int)(string)$shape->getXForm()->getHeight()->getValue());

}

$i += 1;

}

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."SetShapeHeightAndWidth.vdx",$saveFileFormat->VDX);

print "Set height and width of shape.".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Bir Şeklin Yüksekliğini ve Genişliğini Ayarlama (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/SetShapeHeightAndWidth.php)
