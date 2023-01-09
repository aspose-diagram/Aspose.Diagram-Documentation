---
title: Kontrollera närvaron av en master i Visio-ritningen i PHP
type: docs
weight: 10
url: /sv/java/check-presence-of-a-master-in-the-visio-drawing-in-php/
---
## **Aspose.Diagram - Kontrollera en masternärvaro med ID**
 För att kontrollera en masternärvaro med ID med hjälp av**Aspose.Diagram Java för PHP** , ringa upp**check_presence_master_by_id** metod av**CheckPresenceOfMaster** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Aspose.Diagram - Kontrollera en masternärvaro efter namn**
 För att kontrollera en masternärvaro efter namn med hjälp av**Aspose.Diagram Java för PHP** , ringa upp**check_presence_master_by_name** metod av**CheckPresenceOfMaster** modul. Här kan du se exempelkod.

**PHP-kod**

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
## **Ladda ner Running Code**
 Ladda ner**Kontrollera närvaron av en master i Visio-ritningen (Aspose.Diagram)**från någon av nedan nämnda webbplatser för social kodning:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/CheckPresenceOfMaster.php)
