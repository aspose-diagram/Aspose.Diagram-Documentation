---
title: PHP'de Visio Sayfa Bilgisini Alın
type: docs
weight: 30
url: /tr/java/retrieve-visio-page-information-in-php/
---
## **Aspose.Diagram - Visio Sayfa Bilgisini Al**
 Kullanarak Visio Sayfa Bilgilerini Almak İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**GetPageInfo** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

# page = diagram.getPages().getPage(page_id)

$page = $diagram->getPages()->getPage(0);

print "Page ID : ".$page->getName().PHP_EOL;

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Sayfa Bilgisini Al (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageInfo.php)
