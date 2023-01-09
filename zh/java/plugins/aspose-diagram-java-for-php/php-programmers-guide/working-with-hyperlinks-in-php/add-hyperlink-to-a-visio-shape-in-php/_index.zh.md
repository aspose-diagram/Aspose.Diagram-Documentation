---
title: 在 PHP 中将超链接添加到 Visio 形状
type: docs
weight: 10
url: /zh/java/add-hyperlink-to-a-visio-shape-in-php/
---
## **Aspose.Diagram - 添加超链接**
添加超链接使用**Aspose.Diagram Java 用于 PHP** 只需调用**添加超链接到形状**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "Drawing.vsd");

\# Initialize Hyperlink object

$hyperlink = new Hyperlink();

\# Set address value

$hyperlink->getAddress()->setValue("http://www.google.com/");

\# Set sub address value

$hyperlink->getSubAddress()->setValue("Sub address here");

\# Set description value

$hyperlink->getDescription()->setValue("Description here");

\# Set name

$hyperlink->setName("MyHyperLink");

\# Add hyperlink to the shape

$diagram->getPages()->getPage("Flow 1")->getShapes()->getShape(1)->getHyperlinks()->add($hyperlink);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir . "Hyperlinks.vdx", $saveFileFormat->VDX);

print "Added hyperlik to shape successfully!".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**将超链接添加到 Visio 形状 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithHyperlinks/AddHyperlinkToShape.php)
