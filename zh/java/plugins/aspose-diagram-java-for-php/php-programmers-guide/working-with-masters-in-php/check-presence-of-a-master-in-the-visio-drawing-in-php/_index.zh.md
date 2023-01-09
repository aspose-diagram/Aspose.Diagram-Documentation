---
title: 用 PHP 检查 Visio 绘图中是否存在大师
type: docs
weight: 10
url: /zh/java/check-presence-of-a-master-in-the-visio-drawing-in-php/
---
## **Aspose.Diagram - 通过 ID 检查主存在**
要通过 ID 检查主状态，请使用**Aspose.Diagram Java 用于 PHP**， 称呼**check_presence_master_by_id**的方法**CheckPresenceOfMaster**模块。在这里您可以看到示例代码。

**PHP代码**

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
## **Aspose.Diagram - 按名称检查主状态**
要按名称检查主状态，请使用**Aspose.Diagram Java 用于 PHP**， 称呼**check_presence_master_by_name**的方法**CheckPresenceOfMaster**模块。在这里您可以看到示例代码。

**PHP代码**

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
## **下载运行代码**
下载**检查 Visio 绘图中是否存在大师 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/CheckPresenceOfMaster.php)
