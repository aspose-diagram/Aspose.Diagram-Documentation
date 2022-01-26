---
title: Get Master Object from Drawing in PHP
type: docs
weight: 20
url: /java/get-master-object-from-drawing-in-php/
---

## **Aspose.Diagram - Getting a Master Object by ID**
To Get a Master Object by ID using **Aspose.Diagram Java for PHP**, call **get_master_object_by_id** method of **GetMasterObject** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

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
## **Aspose.Diagram - Getting a Master Object by Name**
To Get a Master Object by Name using **Aspose.Diagram Java for PHP**, call **get_master_object_by_name** method of **GetMasterObject** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

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
## **Download Running Code**
Download **Get Master Object from Drawing (Aspose.Diagram)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterObject.php)
