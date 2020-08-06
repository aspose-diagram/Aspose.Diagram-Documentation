---
title: Check Presence of a Master in the Visio Drawing in PHP
type: docs
weight: 10
url: /java/check-presence-of-a-master-in-the-visio-drawing-in-php/
---

## **Aspose.Diagram - Checking a Master Presence by ID**
To Check a Master Presence by ID using **Aspose.Diagram Java for PHP**, call **check_presence_master_by_id** method of **CheckPresenceOfMaster** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 public static function check_presence_master_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$master_id = 2;

\# check master by id

$is_present = $diagram->getMasters()->isExist($master_id);

print "Master Presence : ".(string)$is_present.PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - Checking a Master Presence by Name**
To Check a Master Presence by Name using **Aspose.Diagram Java for PHP**, call **check_presence_master_by_name** method of **CheckPresenceOfMaster** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

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
## **Download Running Code**
Download **Check Presence of a Master in the Visio Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/CheckPresenceOfMaster.php)
- [CodePlex](https://asposediagramjavaphp.codeplex.com/SourceControl/latest#src/aspose/diagram/WorkingwithMasters/CheckPresenceOfMaster.php)
