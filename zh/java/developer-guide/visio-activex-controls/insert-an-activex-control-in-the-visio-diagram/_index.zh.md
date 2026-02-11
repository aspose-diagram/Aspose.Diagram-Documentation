---
title: Insert an ActiveX Control in the Visio Diagram
type: docs
weight: 10
url: /zh/java/insert-an-activex-control-in-the-visio-diagram/
---
{{% alert color="primary" %}}

开发者可以直接在Microsoft Visio 绘图中添加ActiveX控件，使Visio diagram 交互使用[Aspose.Diagram for Java API](https://products.aspose.com/diagram/java/).

{{% /alert %}}
## **插入 ActiveX 控件编程示例**
[页](https://reference.aspose.com/diagram/java/com.aspose.diagram/page)类提供 addActiveXControl 方法并允许开发人员插入任何类型的 ActiveX 控件，如命令按钮、组合框、复选框、列表框、文本框、旋转按钮、单选按钮、标签、图像、切换按钮和滚动条。

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(InsertanActiveControl.class) + "VisioActiveXControls/";
// Instantiate Diagram Object
Diagram diagram = new Diagram();
// Insert an ActiveX control
diagram.getPages().get(0).addActiveXControl(ControlType.IMAGE, 1, 1, 1, 1);
// Save diagram
diagram.save(dataDir + "InsertActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
