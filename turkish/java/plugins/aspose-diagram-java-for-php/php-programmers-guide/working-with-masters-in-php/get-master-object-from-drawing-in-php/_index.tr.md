---
title: PHP'de Çizimden Ana Nesneyi Alın
type: docs
weight: 20
url: /tr/java/get-master-object-from-drawing-in-php/
---
## **Aspose.Diagram - Kimliğe Göre Ana Nesne Alma**
 Kullanarak kimliğe göre bir Ana Nesne Almak için**PHP için Aspose.Diagram Java** , aramak**get_master_object_by_id** yöntemi**GetMasterObject** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 public static function get_master_object_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$master_id = 2;

\# Get master object by id

$master = $diagram->getMasters()->getMaster($master_id);

print "Master ID : ".(string)$master->getID().PHP_EOL;

print "Master Name : ".(string)$master->getName().PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Ada Göre Ana Nesne Alma**
 Kullanarak Ada Göre Bir Ana Nesne Almak İçin**PHP için Aspose.Diagram Java** , aramak**get_master_object_by_name** yöntemi**GetMasterObject** modül. Burada örnek kodu görebilirsiniz.

**PHP Kodu**

{{< highlight "php" >}}

 public static function get_master_object_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Set master name

$master_name = "Background tranquil .2";

\# Get master object by name

$master = $diagram->getMasters()->getMasterByName($master_name);

print "Master ID : ".(string)$master->getID().PHP_EOL;

print "Master Name : ".(string)$master->getName().PHP_EOL;

}

{{< /highlight >}}
## **Çalışan Kodu İndir**
 İndirmek**Çizimden Ana Nesneyi Al (Aspose.Diagram)**aşağıda belirtilen sosyal kodlama sitelerinin herhangi birinden:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterObject.php)
