---
title: 使用图像
type: docs
weight: 70
url: /zh/python-java/working-with-images/
description: 本页介绍如何使用 Aspose.Diagram 库从 Visio 绘图的页面中提取、替换或插入图像。
---
## **从 Visio 页面中提取所有图像**
在 Microsoft Visio 中，页面要么是前景页面，要么是背景页面。您可以从特定页面中提取图像[一个 Visio 文件](ExtractAllImagesFromPage.vsd).
### **提取图像**
Page Class 对象表示前景页面或背景页面的绘图区域。 Diagram 类公开的 Shapes 属性支持 Aspose.Diagram.Shape 对象的集合。此属性可用于从特定页面中提取所有图像。
#### **提取图像编程示例**
以下代码从特定的 Visio 页面中提取所有图像。

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Shapes-IconAndPictures-ExtractAllImagesFromPage.py" >}}
## **获取各种 Visio 形状的图标**
Aspose.Diagram for Python via Java API 现在允许开发者获取各种图标[Visio 形状](Timeline.vss). 
### **获取形状图标**
下面示例中的代码显示了如何：

1. 加载现有的 diagram 或模板。
1. 通过索引掌握
1. 获取主图标。
1. 将图标保存到本地空间。
#### **获取图标编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Shapes-IconAndPictures-GetShapeIcon.py" >}}
## **替换Visio Diagram的图片形状**
Aspose.Diagram for Python via Java API 允许开发人员访问和替换可用的图片形状[Visio diagram](ExtractAllImagesFromPage.vsd).
### **替换图片形状**
下面示例中的代码显示了如何：

1. 加载现有的 diagram。
1. 遍历选择性页面形状。
1. 应用过滤器以获得图片形状。
1. 将结果 Visio diagram 保存到本地空间。
#### **替换图片形状编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Shapes-IconAndPictures-ReplaceShapePicture.py" >}}
## **将图像导入为 Visio 形状**
Aspose.Diagram for Python via Java API 现在允许开发人员将图像导入为 Microsoft Visio 形状。
### **在 Visio 中插入图像**
下面示例中的代码显示了如何：

1. 创建一个 diagram。
1. 获取 Visio 页
1. 将图像导入为 Visio 形状
1. 保存 diagram。
#### **插入图像编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Shapes-IconAndPictures-InsertImageInVisio.py" >}}
