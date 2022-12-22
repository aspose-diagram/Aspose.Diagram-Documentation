---
title: PHP'de Visio Çiziminden Sayfa Nesnesi Alın
type: docs
weight: 10
url: /tr/java/get-a-page-object-from-visio-drawing-in-php/
---
## **Aspose.Diagram - Kimliğe Göre Sayfa Nesnesi Alma**
 Kullanarak kimliğe göre bir Sayfa Nesnesi Almak için**PHP için Aspose.Diagram Java** , aramak**get_page_object_by_id** yöntemi**GetPageObject** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 public static function get_page_object_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$page_id = 0;

\# Get page object by id

$page = $diagram->getPages()->getPage($page_id);

print "Page : ".(string)$page.PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Ada Göre Sayfa Nesnesi Alma**
 Kullanarak Ada Göre Sayfa Nesnesi Almak İçin**PHP için Aspose.Diagram Java** , aramak**get_page_object_by_name** yöntemi**GetPageObject** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 public static function get_page_object_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Set page name

$page_name = "Flow 1";

\# Get page object by name

$page = $diagram->getPages()->getPage($page_name);

print "Page : ".(string)$page.PHP_EOL;

}

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Çiziminden (Aspose.Diagram) Sayfa Nesnesi Alın**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageObject.php)
