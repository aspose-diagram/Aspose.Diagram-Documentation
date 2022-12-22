---
title: PHP'de Visio Çiziminde Master Varlığını Kontrol Edin
type: docs
weight: 10
url: /tr/java/check-presence-of-a-master-in-the-visio-drawing-in-php/
---
## **Aspose.Diagram - Kimliğe Göre Bir Ana Varlığın Kontrol Edilmesi**
 Kimliğe göre bir Ana Varlığı Kontrol Etmek İçin**PHP için Aspose.Diagram Java** , aramak**check_presence_master_by_id** yöntemi**CheckPresenceOfMaster** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 public static function check_presence_master_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$master_id = 2;

\# check master by id

$is_present = $diagram->getMasters()->isExist($master_id);

print "Master Presence : ".(string)$is_present.PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Ada Göre Bir Ana Varlığın Kontrol Edilmesi**
 Bir Ana Varlığı Ada Göre Kontrol Etmek İçin**PHP için Aspose.Diagram Java** , aramak**check_presence_master_by_name** yöntemi**CheckPresenceOfMaster** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 public static function check_presence_master_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Set master name

$master_name = "Background tranquil .2";

\# check master object by name

$is_present = $diagram->getMasters()->isExist($master_name);

print "Master Presence : ".(string)$is_present.PHP_EOL;

}

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Visio Çiziminde Master Varlığını Kontrol Edin (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/CheckPresenceOfMaster.php)
