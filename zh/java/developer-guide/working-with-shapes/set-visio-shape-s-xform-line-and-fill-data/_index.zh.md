---
title: 设置 Visio Shape 的 XForm、Line 和 Fill 数据
type: docs
weight: 70
url: /zh/java/set-visio-shape-s-xform-line-and-fill-data/
---
## **设置变形数据**
XForm 元素是 Microsoft Visio XML 模式的一部分。 XForm 指定形状位置，例如宽度、高度、旋转以及形状是否已翻转。这[变形](https://reference.aspose.com/diagram/java/com.aspose.diagram/xform)财产，由暴露[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)类，支持 Aspose.Diagram.XForm 对象。 XForm 属性可用于检索或更新形状的 XForm 数据。本文中的代码示例更改 PinX（X 坐标）和 PinY（Y 坐标）XForm 值以移动页面上的形状。

**输入 diagram** 

![待办事项：图片_替代_文本](set-visio-shape-s-xform-line-and-fill-data_1.png)

**diagram后** **品X** **和** **拼音** **值已更改** 

![待办事项：图片_替代_文本](set-visio-shape-s-xform-line-and-fill-data_2.png)

更新 XForm 数据的过程是：

1. 加载 diagram。# 查找特定形状。# 更新形状的 XForm 数据。
1. 保存 diagram。
### **编程范例**
下面的代码片段显示了如何更新形状的 XForm 数据。代码查找形状名称进程，形状 ID 为 1，并将其 X 和 Y 坐标设置为 5。


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetXFormdata.class); 
// call a Diagram class constructor to load the VSD diagram
Diagram diagram = new Diagram(dataDir + "SetXFormdata.vsd");

//Find a particular shape and update its XForm
for(Shape shape :(Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "process" && shape.getID() == 1)
    {
        shape.getXForm().getPinX().setValue(5);
        shape.getXForm().getPinY().setValue(5);
    }
}
// save diagram
diagram.save(dataDir + "SetXFormdata_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **设置 Visio 形状的线数据**
可以通过多种方式格式化形状。本文介绍如何指定线条的属性。

Microsoft Visio 允许用户以各种方式格式化行。 Aspose.Diagram for Java 支持：

- 权重：一条线的粗细。
- 颜色：设置形状的线条颜色。
- 线条颜色透明度：以百分比设置形状的线条颜色透明度。
- 图案：定义线条是实线、虚线还是其他图案。
- 圆角：角的半径。
- 开始和结束箭头：指定行是否有箭头。
- 开始和结束箭头大小：设置箭头大小。
- Cap：线的圆角结束。
### **更改形状边框的线条颜色、粗细、破折号类型、透明度、圆角、箭头类型和箭头大小**
这[线](https://reference.aspose.com/diagram/java/com.aspose.diagram/line)财产，由暴露[形状](https://reference.aspose.com/diagram/java/com.aspose.diagram/shape)类，支持 Aspose.Diagram.Line 对象。此属性可用于检索或更新形状的线条数据。
#### **线路数据编程示例**
下面的一段代码更新形状的线数据。


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetLineData.class);

// load a Visio diagram
Diagram diagram = new Diagram(dataDir + "SetLineData.vsd");
// get the page by its name
Page page1 = diagram.getPages().getPage("Page-1");
// get shape by its ID
Shape shape = page1.getShapes().getShape(1);
// set line dash type by index
shape.getLine().getLinePattern().setValue(4);
// set line weight, defualt in PT
shape.getLine().getLineWeight().setValue(2);
// set color of the shape's line
shape.getLine().getLineColor().getUfe().setF("RGB(95,108,53)");
// set line rounding, default in inch
shape.getLine().getRounding().setValue(0.3125);
// set line caps
shape.getLine().getLineCap().setValue(BOOL.TRUE);
// set line color transparency in percent
shape.getLine().getLineColorTrans().setValue(50);

/* add arrows to the connector or curve shapes */
// select arrow type by index
shape.getLine().getBeginArrow().setValue(4);
shape.getLine().getEndArrow().setValue(4);
// set arrow size 
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);
shape.getLine().getBeginArrowSize().setValue(ArrowSizeValue.LARGE);

// save the Visio
diagram.save(dataDir + "SetLineData_Out.vsdx", SaveFileFormat.VSDX);
// save diagram
diagram.save(dataDir+ "output.vdx", SaveFileFormat.VDX);

{{< /highlight >}}

## **设置 Visio 形状的填充数据**
可以通过多种方式格式化形状。本主题介绍如何指定形状的填充。

 Microsoft Office Visio 允许用户以各种方式填写格式。这[充满](https://reference.aspose.com/diagram/java/com.aspose.diagram/fill)Aspose.Diagram for Java API 类支持设置：

- 背景和前景色。
- 透明度。
- 填充图案。
- 阴影。
### **设置填充值**
Shape 类公开的 Fill 属性支持 Aspose.Diagram.Fill 对象。 Fill 属性可用于检索或更新形状的填充数据。

|<p>**输入diagram** </p><p>![待办事项：图片_替代_文本](http://i.imgur.com/OrhEecb.png)</p>|<p>**更改填充颜色后的diagram** </p><p>![待办事项：图片_替代_文本](http://i.imgur.com/HO0wmZ8.png)</p>|
|:- |:- |
#### **填充数据编程示例**
以下代码片段更新形状的填充数据。该代码查找名为 rectangle 且形状 ID 为 1 的形状，并设置填充背景和前景色。


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetFillData.class);


//Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir+ "Drawing1.vsd");

//Find a particular shape and update its XForm
for (com.aspose.diagram.Shape shape : (Iterable<Shape>) diagram.getPages().get(0).getShapes())
{
    if (shape.getNameU().toLowerCase() == "rectangle" && shape.getID() == 1)
    {
        shape.getFill().getFillBkgnd().setValue(diagram.getPages().getPage(0).getShapes().getShape(0).getFill().getFillBkgnd().getValue());
        shape.getFill().getFillForegnd().setValue("#ebf8df");
    }
}
// save diagram
diagram.save(dataDir+ "SetFillData_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

### **检索 Visio 形状的继承填充数据**
Visio 形状可以继承父样式和主形状。开发者可以获取或设置一个Visio形状的继承填充数据。 Shape 类公开的 InheritFill 属性包含由父样式和主控形状继承的形状的填充格式值。
#### **检索继承的填充数据编程示例**
以下代码片段检索形状的继承填充数据。请检查此示例代码：


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getSharedDataDir(RetrieveInheritedFillData.class) + "Shapes/";

// Call the diagram constructor to load a VSDX diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Get page by ID
Page page = diagram.getPages().getPage("Page-1");
// Get shape by ID
Shape shape = page.getShapes().getShape(1);
// Get the fill formatting values
System.out.println(shape.getInheritFill().getFillBkgnd().getValue());
System.out.println(shape.getInheritFill().getFillForegnd().getValue());
System.out.println(shape.getInheritFill().getFillPattern().getValue());
System.out.println(shape.getInheritFill().getShapeShdwObliqueAngle().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetX().getValue());
System.out.println(shape.getInheritFill().getShapeShdwOffsetY().getValue());
System.out.println(shape.getInheritFill().getShapeShdwScaleFactor().getValue());
System.out.println(shape.getInheritFill().getShapeShdwType().getValue());
System.out.println(shape.getInheritFill().getShdwBkgnd().getValue());
System.out.println(shape.getInheritFill().getShdwBkgndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwForegnd().getValue());
System.out.println(shape.getInheritFill().getShdwForegndTrans().getValue());
System.out.println(shape.getInheritFill().getShdwPattern().getValue());

{{< /highlight >}}

