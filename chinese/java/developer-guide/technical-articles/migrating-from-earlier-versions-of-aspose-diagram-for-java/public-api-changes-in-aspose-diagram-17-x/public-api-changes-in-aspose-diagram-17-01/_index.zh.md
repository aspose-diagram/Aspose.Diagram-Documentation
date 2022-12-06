---
title: 公共 API Aspose.Diagram 17.01 的变化
type: docs
weight: 10
url: /zh/java/public-api-changes-in-aspose-diagram-17-01/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 16.12.0 到 17.01 的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
### **转换具有选择形状的绘图 Visio**
开发人员可以选择特定的形状将 Visio 绘图转换为任何其他受支持的格式。为此，我们在 RenderingSaveOptions 类中添加了 Shapes 成员。每个保存选项类都是 RenderingSaveOptions 类的扩展形式。请检查代码示例：

**Java**

{{< highlight "csharp" >}}

 // The path to the documents directory.

String dataDir = Utils.getSharedDataDir(ConvertVisioWithSelectiveShapes.class) + "LoadSaveConvert\\";

// call the diagram constructor to load diagram from a VSD file

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class

SVGSaveOptions options = new SVGSaveOptions();

ShapeCollection shapes = options.getShapes();

// get shapes by page index and shape ID, and then add in the shape collection object

shapes.add(diagram.getPages().get(0).getShapes().getShape(1));

shapes.add(diagram.getPages().get(0).getShapes().getShape(2));

// save Visio drawing

diagram.save(dataDir + "SelectiveShapes_out.svg", options);

{{< /highlight >}}
