---
title: 在 PHP 中检索硕士信息
type: docs
weight: 30
url: /zh/java/retrieve-the-masters-information-in-php/
---
## **Aspose.Diagram - 检索大师信息**
使用检索大师信息**Aspose.Diagram Java 用于 PHP** 只需调用**获取MasterInfo**模块。在这里您可以看到示例代码。

**PHP代码**

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
## **下载运行代码**
下载**检索大师信息 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithMasters/GetMasterInfo.php)
