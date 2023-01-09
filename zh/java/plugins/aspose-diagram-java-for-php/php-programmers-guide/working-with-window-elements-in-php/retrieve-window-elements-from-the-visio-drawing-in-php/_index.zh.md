---
title: 在 PHP 中从 Visio 绘图中检索窗口元素
type: docs
weight: 30
url: /zh/java/retrieve-window-elements-from-the-visio-drawing-in-php/
---
## **Aspose.Diagram - 从 Visio 绘图中检索窗口元素**
要从 Visio 绘图中检索窗口元素，请使用**Aspose.Diagram Java 用于 PHP** 只需调用**获取窗口元素**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$windows=$diagram->getWindows();

$i = 0;

while ($i<(int)(string)$windows->getCount()) {

$window=$windows->get($i);

print "ID: ".(string)$window->getID();

print "Type: ".(string)$window->getWindowType();

print "Window height: ".(string)$window->getWindowHeight();

print "Window width: ".(string)$window->getWindowWidth();

print"Window state: ".(string)$window->getWindowState();

$i+= 1;

}

{{< /highlight >}}
## **下载运行代码**
下载**从 Visio 绘图中检索窗口元素 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/GetWindowElements.php)
