---
title: 公共 API Aspose.Diagram 6.8.0 的变化
type: docs
weight: 10
url: /zh/java/public-api-changes-in-aspose-diagram-6-8-0/
---
{{% alert color="primary" %}} 

本文档描述了 Aspose.Diagram API 从版本 6.7.0 到 6.8.0 的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.Diagram 中幕后行为的任何更改的描述。

{{% /alert %}} 
### **插入 ActiveX 控件**
开发者可以在Visio diagram插入一个ActiveX控件，我们在[页](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/Page)班级。请检查此代码示例：

**Java**

{{< highlight "java" >}}

 // load an existing Visio diagram

Diagram diagram = new Diagram();

// insert an ActiveX control

diagram.getPages().get(0).addActiveXControl(ControlType.IMAGE, 1, 1, 1, 1);

// save diagram

diagram.save("C:\\temp\\MyOutput.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **设置图层的颜色复选框**
开发者可以使用 Aspose.Diagram API 来设置或获取Layer的Color CheckBox，请查看此代码示例：

**Java**

{{< highlight "java" >}}

 // Load source Visio diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// Get Visio page

Page page = diagram.getPages().getPage("Page-1");

// Initialize a new Layer class object

Layer layer = new Layer();

// set Layer name

layer.getName().setValue("Layer1");

// Set Layer Visibility

layer.getVisible().setValue(BOOL.TRUE);

// set the color checkbox of Layer

layer.setColorChecked(BOOL.TRUE);

// Add Layer to the particular page sheet

page.getPageSheet().getLayers().add(layer);

// get shape by ID

Shape shape = page.getShapes().getShape(3);

// assign shape to this new Layer

shape.getLayerMem().getLayerMember().setValue(Integer.toString(layer.getIX()));

// save diagram

diagram.save("c:\\temp\\AddLayer_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
### **在 Shape 类中添加 InheritFill 属性**
开发人员可以获取或设置继承填充属性。我们在 Shape 类中添加了 InheritFill 属性。请检查此代码示例：

**Java**

{{< highlight "java" >}}

 // call the diagram constructor to load a VSDX diagram

Diagram diagram = new Diagram("c:\\temp\\Drawing1.vsdx");

// get page by ID

Page page = diagram.getPages().getPage("Page-1");

// get shape by ID

Shape shape = page.getShapes().getShape(1);

// get the fill formatting values

System.out.println(shape.getInheritFill().getFillBkgnd().getValue());

System.out.println(shape.getInheritFill().getFillForegnd().getValue());

System.out.println(shape.getInheritFill().getFillPattern().getValue());

{{< /highlight >}}
