---
title: Bir Şekli PHP'de Uygun Açıyla Döndürün
type: docs
weight: 80
url: /tr/java/rotate-a-shape-with-suitable-angle-in-php/
---
## **Aspose.Diagram - Bir Şekli Uygun Açıyla Döndür**
 Kullanarak Bir Şekli Uygun Açıyla Döndürmek İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**Şekli Döndür** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram=new Diagram($dataDir."Drawing.vsd");

\# Add a shape and set the angle

$diagram->getPages()->getPage(0)->getShapes()->getShape(1)->setAngle(190);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."RotateShape.vdx",$saveFileFormat->VDX);

print "Rotated shape.".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Bir Şekli Uygun Açıyla Döndürün (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/RotateShape.php)
