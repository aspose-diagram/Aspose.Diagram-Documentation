---
title: PHP'de Visio Bağlayıcı Bilgilerini Alın
type: docs
weight: 50
url: /tr/java/retrieve-visio-connectors-information-in-php/
---
## **Aspose.Diagram - Visio Konnektör Bilgilerini Alın**
 Kullanarak Visio Konnektör Bilgilerini Almak İçin**PHP için Aspose.Diagram Java** , sadece çağırmak**GetConnectorsInfo** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$connectors = $diagram->getPages()->getPage(0)->getConnects();

$i = 0;

while ($i<sizeof($connectors->getCount())) {

$connector =$connectors->get($i);

\# Display information about the Connectors

print "From Shape ID : ".(string)$connector->getFromSheet().PHP_EOL;

print "To Shape ID : ".(string)$connector->getToSheet().PHP_EOL;

$i+=1;

}

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Konnektör Bilgilerini Alın (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetConnectorsInfo.php)
