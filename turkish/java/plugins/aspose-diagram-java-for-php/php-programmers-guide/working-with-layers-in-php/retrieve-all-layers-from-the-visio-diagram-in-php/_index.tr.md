---
title: PHP'de Visio Diagram'den Tüm Katmanları Alın
type: docs
weight: 20
url: /tr/java/retrieve-all-layers-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - Tüm Katmanları Al**
 Kullanarak Tüm Katmanları Almak İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**Tüm Katmanları Getir** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "Drawing.vsd");

\# get Visio page

$page=$diagram->getPages()->getPage(0);

$layers=$page->getPageSheet()->getLayers();

$i = 0;

while ($i<(int)(string)$layers->getCount()) {

$layer=$layers->get($i);

print "Name: " . (string)$layer->getName()->getValue();

print "Visibility: " . (string)$layer->getVisible()->getValue();

print "Status: " . (string)$layer->getStatus()->getValue();

$i += 1;

}

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Diagram'den (Aspose.Diagram) Tüm Katmanları Alın**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithLayers/GetAllLayers.php)
