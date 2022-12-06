---
title: PHP'deki Visio Sayfasındaki Tüm Resimleri Çıkarın
type: docs
weight: 30
url: /tr/java/extract-all-images-from-a-visio-page-in-php/
---
## **Aspose.Diagram - Bir Visio Sayfasından Tüm Resimleri Çıkarın**
 Kullanarak Visio Sayfasından Tüm Görüntüleri Çıkarmak için**PHP için Aspose.Diagram Java** , sadece çağırmak**Görüntüleri Ayıkla** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

$shapes = $diagram->getPages()->getPage("Flow 1")->getShapes();

$i = 0;

$typeValue=new TypeValue();

while ($i <(int)(string)$shapes->getCount()){

$shape = $shapes->get($i);

\# Filter shapes by type Foreign

if ($shape->getType()== $typeValue->FOREIGN){

\# create an image file

$fos = new FileOutputStream($dataDir."Image#{i}.bmp");

$fos->write($shape->getForeignData()->getValue());

$fos->close();

}

$i += 1;

}

print "Extracted images successfully!".PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Bir Visio Sayfasından Tüm Resimleri Çıkarın (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithShapes/ExtractImages.php)
