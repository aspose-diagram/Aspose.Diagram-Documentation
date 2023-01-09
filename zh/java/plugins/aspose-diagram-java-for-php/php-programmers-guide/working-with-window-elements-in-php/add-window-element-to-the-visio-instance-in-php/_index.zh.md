---
title: 在 PHP 中将窗口元素添加到 Visio 实例
type: docs
weight: 20
url: /zh/java/add-window-element-to-the-visio-instance-in-php/
---
## **Aspose.Diagram - 将窗口元素添加到 Visio 实例**
将窗口元素添加到 Visio 实例使用**Aspose.Diagram Java 用于 PHP** 只需调用**添加窗口元素**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# initialize window object

$window = new Window();

\# set window state

$windowStateValue=new WindowStateValue();

$window->setWindowState($windowStateValue->MAXIMIZED);

\# set window height

$window->setWindowHeight(500);

\# set window width

$window->setWindowWidth(500);

\# set window type

$windowTypeValue=new WindowTypeValue();

$window->setWindowType($windowTypeValue->STENCIL);

\# add window object

$diagram->getWindows()->add($window);

\# save in any supported format

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddWindowElement.vdx", $saveFileFormat->VDX);

print "Added window element to the visio instance.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**将窗口元素添加到 Visio 实例 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/AddWindowElement.php)
