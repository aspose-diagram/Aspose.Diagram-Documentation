---
title: 从形状对象中检索 ActiveX 控件以修改属性
type: docs
weight: 20
url: /zh/java/retrieve-an-activex-control-from-a-shape-object-to-modify-properties/
---
{{% alert color="primary" %}} 

使用 Aspose.Diagram API，开发人员可以从 Visio 形状对象中检索 ActiveX 控件以设置其所有可用属性。

{{% /alert %}} 
## **检索 ActiveX 控件编程示例**
[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)类提供 getActiveXControl 方法，允许开发人员从 Visio 形状对象检索 ActiveX 控件。开发人员可以在适当的 ActiveX 控件类中转换一个 ActiveX 控件，然后设置它的所有可用属性。

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveActiveXControl.class) + "VisioActiveXControls/";
// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsd");
// get a Visio page by name
Page page = diagram.getPages().getPage("Page-1");
// get a shape by ID
Shape shape = page.getShapes().getShape(1);
// get an ActiveX control
CommandButtonActiveXControl cbac = (CommandButtonActiveXControl)shape.getActiveXControl();
// set width of the command button control
cbac.setWidth(4);
// set height of the command button control
cbac.setHeight(4);
// set caption of the command button control
cbac.setCaption("Test Button");
// save diagram
diagram.save(dataDir + "RetrieveActiveXControl_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
