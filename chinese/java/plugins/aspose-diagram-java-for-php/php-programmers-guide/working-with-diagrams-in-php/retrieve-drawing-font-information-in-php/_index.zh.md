---
title: 在 PHP 中检索绘图字体信息
type: docs
weight: 40
url: /zh/java/retrieve-drawing-font-information-in-php/
---
## **Aspose.Diagram - 检索绘图字体信息**
要使用检索绘图字体信息**Aspose.Diagram Java 用于 PHP** 只需调用**获取图表字体信息**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

$fonts = $diagram->getFonts();

$i = 0;

while ($i<sizeof($fonts->getCount())) {

$font = $fonts->get($i);

\# Display information about the fonts

print $font->getName();

$i+=1;

}

{{< /highlight >}}
## **下载运行代码**
下载**检索绘图字体信息 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetDiagramFontInfo.php)
