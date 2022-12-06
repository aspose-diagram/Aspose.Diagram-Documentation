---
title: 使用图像
type: docs
weight: 60
url: /zh/net/working-with-images/
description: 本节介绍如何使用 Aspose.Diagram 从 visio 页面插入或获取图像。
---
## **从 Visio 页面中提取所有图像**
在 Microsoft Visio 中，页面要么是前景页面，要么是背景页面。您可以从 Visio 文件的特定页面中提取图像。
### **提取图像**
Page Class 对象表示前景页面或背景页面的绘图区域。 Diagram 类公开的 Shapes 属性支持 Aspose.Diagram.Shape 对象的集合。此属性可用于从特定页面中提取所有图像。
#### **提取图像编程示例**
以下代码从特定的 Visio 页面中提取所有图像。

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ExtractAllImagesFromPage-ExtractAllImagesFromPage.cs" >}}
## **获取各种 Visio 形状的图标**
Aspose.Diagram for .NET API 现在允许开发者获取各种 Visio 形状的图标。
### **获取形状图标**
下面示例中的代码显示了如何：

1. 加载现有的 diagram 或模板。
1. 通过索引掌握
1. 获取主图标。
1. 将图标保存到本地空间。
#### **获取图标编程示例**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-GetShapeIcon-GetShapeIcon.cs" >}}
## **替换Visio Diagram的图片形状**
Aspose.Diagram for .NET API 允许开发人员访问和替换 Visio diagram 中可用的图片形状。
### **替换图片形状**
下面示例中的代码显示了如何：

1. 加载现有的 diagram。
1. 遍历选择性页面形状。
1. 应用过滤器以获得图片形状。
1. 将结果 Visio diagram 保存到本地空间。
#### **替换图片形状编程示例**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-ReplaceShapePicture-ReplaceShapePicture.cs" >}}
## **将位图图像导入为 Visio 形状**
Aspose.Diagram for .NET API 现在允许开发人员将位图图像导入为 Microsoft Visio 形状。
### **在 Visio 中插入 BMP 图片**
下面示例中的代码显示了如何：

1. 创建一个 diagram。
1. 获取 Visio 页
1. 将位图图像导入为 Visio 形状
1. 保存 diagram。
#### **插入 BMP 图像编程示例**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Shapes-Working-with-Icons-and-Pictures-InsertImageInVisio-InsertImageInVisio.cs" >}}
## **将Visio页面的指定区域转换为图片**
通过Aspose.Diagram for .NET API，开发者可以定义一个XY坐标、宽度和高度的区域，然后将这个区域转换为支持的图像格式。
### **将 Visio 绘图区域转换为图像**
下面示例中的代码显示了如何：

1. 加载现有的 Visio 图纸
1. 定义矩形区域
1. 将指定区域转换为图像

**C#**

{{< highlight "java" >}}

 // load a Visio drawing

Diagram diagram = new Diagram(@"c:\temp\Drawing1.vsdx");

Aspose.Diagram.Saving.ImageSaveOptions Options = new Aspose.Diagram.Saving.ImageSaveOptions(SaveFileFormat.PNG);

// specify region with XY coordinates, width and height

Options.Area = new RectangleF(0, 0, 1, 1);

// save into the image format

diagram.Save(@"c:\temp\area.png", Options);

{{< /highlight >}}
