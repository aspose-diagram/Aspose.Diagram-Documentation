---
title: Få Master Object från Drawing i PHP
type: docs
weight: 20
url: /sv/java/get-master-object-from-drawing-in-php/
---
## **Aspose.Diagram - Få ett huvudobjekt med ID**
 För att få ett huvudobjekt med ID med hjälp av**Aspose.Diagram Java för PHP** , ringa upp**get_master_object_by_id** metod av**GetMasterObject** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Aspose.Diagram - Få ett huvudobjekt efter namn**
 För att få ett huvudobjekt med namn med hjälp av**Aspose.Diagram Java för PHP** , ringa upp**get_master_object_by_name** metod av**GetMasterObject** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Få huvudobjekt från ritning (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterObject.php)
