---
title: 在 PHP 中检索 Visio 连接器信息
type: docs
weight: 50
url: /zh/java/retrieve-visio-connectors-information-in-php/
---
## **Aspose.Diagram - 检索 Visio 连接器信息**
检索 Visio 连接器信息使用**Aspose.Diagram Java 用于 PHP** 只需调用**获取连接器信息**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$connectors = $diagram->getPages()->getPage(0)->getConnects();

$i = 0;

while ($i<sizeof($connectors->getCount())) {

$connector =$connectors->get($i);

\# Display information about the Connectors

print "From Shape ID : ".(string)$connector->getFromSheet().PHP_EOL;

print "To Shape ID : ".(string)$connector->getToSheet().PHP_EOL;

$i+=1;

}

{{< /highlight >}}
## **下载运行代码**
下载**检索 Visio 连接器信息 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetConnectorsInfo.php)
