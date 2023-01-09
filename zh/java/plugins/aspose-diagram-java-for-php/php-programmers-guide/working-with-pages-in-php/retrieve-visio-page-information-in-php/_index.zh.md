---
title: 在 PHP 中检索 Visio 页面信息
type: docs
weight: 30
url: /zh/java/retrieve-visio-page-information-in-php/
---
## **Aspose.Diagram - 检索 Visio 页面信息**
检索 Visio 页面信息使用**Aspose.Diagram Java 用于 PHP** 只需调用**获取页面信息**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

# page = diagram.getPages().getPage(page_id)

$page = $diagram->getPages()->getPage(0);

print "Page ID : ".$page->getName().PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**检索 Visio 页面信息 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageInfo.php)
