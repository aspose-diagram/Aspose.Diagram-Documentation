---
title: 从 PHP 绘图中获取主对象
type: docs
weight: 20
url: /zh/java/get-master-object-from-drawing-in-php/
---
## **Aspose.Diagram - 通过 ID 获取主对象**
要使用 ID 通过 ID 获取主对象**Aspose.Diagram Java 用于 PHP**， 称呼**get_master_object_by_id 获取**的方法**获取主对象**模块。在这里您可以看到示例代码。

**PHP代码**

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
## **Aspose.Diagram - 按名称获取主对象**
要按名称获取主对象，请使用**Aspose.Diagram Java 用于 PHP**， 称呼**get_master_object_by_name**的方法**获取主对象**模块。在这里您可以看到示例代码。

**PHP代码**

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
## **下载运行代码**
下载**从绘图中获取主对象 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterObject.php)
