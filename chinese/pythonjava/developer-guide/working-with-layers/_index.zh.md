---
title: 使用图层
type: docs
weight: 160
url: /zh/python-java/working-with-layers/
---
### **使用图层配置形状对象**
Aspose.Diagram for Python via Java allows to configure shape objects with layers in Microsoft Office Visio diagram. Each shape can belong to multiple layers so developers can manage shapes to suit end user needs.

这[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/Shape)类对象提供 LayerMember 属性，允许在 Visio 绘图的图层中添加/删除形状对象。用户可以使用 Aspose.Diagram API 以编程方式管理这些属性，如下所示：

**在 diagram 的图层中添加、删除和移动形状对象。** 

以下代码有助于添加、删除和移动形状对象属性。
#### **编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-ConfigureShapeLayers.py" >}}
### **在 Visio PageSheet 中添加图层**
Aspose.Diagram for Python via Java allows developers to add new layers to organize custom categories of shapes, and then assign shapes to those layers programmatically.

这[图层集合](https://reference.aspose.com/diagram/java/com.aspose.diagram/LayerCollection)类提供了添加方法，允许添加一个新的[层](https://reference.aspose.com/diagram/java/com.aspose.diagram/layer)中的类对象[Visio图纸](DrawingFlowChart.vsdx).开发者可以通过初始化它的类对象来设置 Layer 的属性。

下面的一段代码有助于添加 Layer 对象。
#### **编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-AddLayer.py" >}}

{{% alert color="primary" %}} 

Aspose.Diagram for Python via Java gives developers access to the existing layers of Visio diagram.

{{% /alert %}} 
### **获取所有可用图层**
这[页表](https://reference.aspose.com/diagram/java/com.aspose.diagram/PageSheet)的财产[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)类允许从中检索可用层的列表[Visio图纸](DrawingFlowChart.vsdx)使用[图层集合](https://reference.aspose.com/diagram/java/com.aspose.diagram/layercollection)班级。

以下代码有助于获取图层列表。
#### **编程示例**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Layers-RetrieveAllLayers.py" >}}
