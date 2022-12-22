---
title: 在 PHP 中从 Visio Diagram 中检索所有图层
type: docs
weight: 20
url: /zh/java/retrieve-all-layers-from-the-visio-diagram-in-php/
---
## **Aspose.Diagram - 检索所有图层**
检索所有图层使用**Aspose.Diagram Java 用于 PHP** 只需调用**获取所有图层**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "Drawing.vsd");

\# get Visio page

$page=$diagram->getPages()->getPage(0);

$layers=$page->getPageSheet()->getLayers();

$i = 0;

while ($i<(int)(string)$layers->getCount()) {

$layer=$layers->get($i);

print "Name: " . (string)$layer->getName()->getValue();

print "Visibility: " . (string)$layer->getVisible()->getValue();

print "Status: " . (string)$layer->getStatus()->getValue();

$i += 1;

}

{{< /highlight >}}
## **下载运行代码**
下载**从 Visio Diagram (Aspose.Diagram) 中检索所有图层**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithLayers/GetAllLayers.php)
