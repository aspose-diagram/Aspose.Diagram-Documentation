---
title: PHP'de Master Bilgilerini Alın
type: docs
weight: 30
url: /tr/java/retrieve-the-masters-information-in-php/
---
## **Aspose.Diagram - Master Bilgilerini Al**
 Kullanarak Master Bilgilerini Almak için**PHP için Aspose.Diagram Java** , sadece çağırmak**GetMasterInfo** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir . "drawing.vsd");

$masters = $diagram->getMasters();

$i = 0;

while ($i<sizeof($masters->getCount())){

$master = $masters->get($i);

print "Master ID : " . (string)$master->getID().PHP_EOL;

print "Master Name : " . (string)$master->getName().PHP_EOL;

$i += 1;

}

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Master Bilgilerini Alın (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterInfo.php)
