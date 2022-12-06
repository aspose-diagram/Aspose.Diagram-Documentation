---
title: 在 PHP 中为 Visio 绘图添加注释
type: docs
weight: 10
url: /zh/java/add-comments-to-visio-drawings-in-php/
---
## **Aspose.Diagram - 为 Visio 图纸添加注释**
使用以下方法向 Visio 工程图添加注释**Aspose.Diagram Java 用于 PHP** 只需调用**添加注释到图表**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Add comment

$diagram->getPages()->getPage(0)->addComment(7.205905511811023, 3.880708661417323, "test@");

\# Save as VDX

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddComment.vdx", $saveFileFormat->VDX);

print "Added comment successfully!".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**添加评论到 Visio 图纸 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/AddCommentToDiagram.php)
