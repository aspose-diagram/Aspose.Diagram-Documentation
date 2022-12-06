---
title: 在 PHP 中从 Visio 绘图中获取页面对象
type: docs
weight: 10
url: /zh/java/get-a-page-object-from-visio-drawing-in-php/
---
## **Aspose.Diagram - 通过 ID 获取页面对象**
要使用 ID 通过 ID 获取页面对象**Aspose.Diagram Java 用于 PHP**， 称呼**get_page_object_by_id**的方法**获取页面对象**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 public static function get_page_object_by_id($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

$page_id = 0;

\# Get page object by id

$page = $diagram->getPages()->getPage($page_id);

print "Page : ".(string)$page.PHP_EOL;

}

{{< /highlight >}}
## **Aspose.Diagram - 按名称获取页面对象**
要按名称获取页面对象，请使用**Aspose.Diagram Java 用于 PHP**， 称呼**get_page_object_by_name**的方法**获取页面对象**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 public static function get_page_object_by_name($dataDir=null){

\# Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Set page name

$page_name = "Flow 1";

\# Get page object by name

$page = $diagram->getPages()->getPage($page_name);

print "Page : ".(string)$page.PHP_EOL;

}

{{< /highlight >}}
## **下载运行代码**
下载**从 Visio 绘图中获取页面对象 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/GetPageObject.php)
